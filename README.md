<h1 align="center" style="line-height:0;">Noise Cancellation</h1>

<div align="center">

<a href="">[![Licence][licence]][licence-url]</a>
<a href="">[![Latest][version]][version-url]</a>

</div>

[licence]: https://img.shields.io/badge/License-GPLv3-blue.svg
[licence-url]: https://www.gnu.org/licenses/gpl-3.0




:exclamation: :exclamation: :exclamation: Do NOT use any other sample rates, use ONLY 48000 Hz, make sure your audio source is 48000 Hz and force it to be 48000 Hz if it is not.

There is a minimalistic GUI with all parameters and diagnostic stats:

<div align="center">
    <img src="https://i.imgur.com/xPkoqlU.png" alt="GUI of the plugin">
</div>



### Plugin Settings

- `VAD Threshold (%)` - if probability of sound being a voice is lower than this threshold - it will be silenced.
  In most cases the threshold between 85% - 95% would be fine.
  Without the VAD some loud noises may still be a bit audible when there is no voice.
- `VAD Grace Period (ms)` - for how long after the last voice detection the output won't be silenced. This helps when ends of words/sentences are being cut off.
- `Retroactive VAD Grace Period (ms)` - similar to `VAD Grace Period (ms)` but for starts of words/sentences. :warning: This introduces latency!

### Windows + Equalizer APO (VST2)

To check or change mic settings go to "Recording devices" -> "Recording" -> "Properties" of the target mic -> "Advanced".

To enable the plugin in Equalizer APO select "Plugins" -> "VST Plugin" and specify the plugin dll.

- Just upload the RNN Plugin in APO and start using.
