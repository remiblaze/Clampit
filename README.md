# Clampit: true-peak mastering limiter

![Clampit free true-peak mastering limiter UI](https://raw.githubusercontent.com/RemiBlaze/Clampit/main/clampit-ui-screenshot.png)

**A clean, loud, streaming-ready ceiling for your master bus.**

Clampit is a lookahead true-peak limiter built to sit last on your master or bus. Set a ceiling your audio can't cross, dial in the release and knee character you want, and check your work with delta monitoring and built-in loudness metering.

**macOS** (Apple Silicon and Intel): AU, VST3, CLAP, AAX, Standalone. Signed and notarized by Apple.

**Windows** 10 and 11, 64-bit: VST3, CLAP, Standalone. Authenticode signed.

AAX ships on macOS only.

---

## 🚀 Download & Install

Go to the [latest release](https://github.com/RemiBlaze/Clampit/releases/latest) and pick your platform.

**macOS**
1. Download **`Clampit_Installer.pkg`**.
2. Double-click it and follow the installer. It is signed and notarized by Apple, so it installs cleanly with no security warnings.
3. Restart your DAW and rescan plug-ins. Clampit appears under **Remi Blaze**.

**Windows 10 and 11, 64-bit**
1. Download **`Clampit_Installer.exe`**.
2. Run it and follow the installer. It is Authenticode signed.
3. Restart your DAW and rescan plug-ins. Clampit appears under **Remi Blaze**.

No dongle and no extra account on either platform.

Full guide: **[remiblaze.com/support](https://remiblaze.com/support/)**.

---

## 🎛️ Features
- **Input**: Drive gain into the limiter (0 to +24 dB).
- **Ceiling**: Output ceiling from -6 dB up to 0 dB; audio never exceeds it.
- **Release**: Manual release from 1 to 1000 ms.
- **Auto Release**: Program-dependent release that adapts to transients versus sustained material.
- **Lookahead**: 0–5 ms of lookahead so the limiter reacts before peaks arrive, with automatic DAW latency compensation.
- **True Peak**: Oversampled (4x) inter-sample peak detection for codec-safe masters.
- **Knee**: Three limiting characters: KNOCK (hard), GLUE (6 dB soft knee), CLOBBER (saturated clip).
- **Stereo Link**: Blend from fully linked (0–100 %) for a stable image down to independent dual-mono limiting.
- **Constant Loudness**: Compensates for input gain so you A/B character, not just level.
- **Delta**: Solo exactly what the limiter is removing.
- **Mono Check**: Sum to mono to audition low-end and phase.
- **Dither**: TPDF dithering at 16-bit or 24-bit for clean bit-depth reduction on export.
- **Bypass**: Loudness-matched bypass for honest comparison.
- **15 factory presets** plus user preset save/load.

---

## 🔬 Under the Hood
- **True-peak detection** via 4x oversampled peak reconstruction, with an internal ceiling margin to absorb inter-sample overshoot.
- **Lookahead delay line** with static latency reporting to the host, so track alignment stays correct, even in bypass.
- **Program-dependent auto-release** driven by crest factor and gain-reduction depth.
- **DC blocker** (5 Hz, double precision) keeps the output symmetric and headroom intact.
- **TPDF dithering** applied as the final audio stage before the output safety limit.
- **Built-in loudness metering** using K-weighted (BS.1770) LUFS measurement.
- **Universal Binary**: native on Apple Silicon and Intel.

---

## 💻 System Requirements

**macOS**
- macOS 15.0 or later
- Apple Silicon or Intel Mac (Universal Binary)
- An AU, VST3, CLAP or AAX host

**Windows**
- Windows 10 or Windows 11, 64-bit
- A VST3 or CLAP host

---

## 🎚️ Factory Presets (15)

| Preset | Input | Ceiling | Best For |
|--------|-------|---------|----------|
| Init | 0 dB | -0.2 dB | Clean starting point |
| Main Stage Master | 0 dB | -0.2 dB | Fast auto-release master |
| Sub-Deep Transparency | 0 dB | -0.2 dB | Sub-heavy material with soft knee |
| Clobber Bus | +6 dB | -0.2 dB | Aggressive, saturated bus limiting |
| Forensic Mono Guard | 0 dB | -0.2 dB | Delta monitoring |
| Transparent Master | 0 dB | -0.3 dB | Maximum-transparency mastering |
| Loud Master | +6 dB | -0.3 dB | Competitive loudness |
| Aggressive | +12 dB | -0.3 dB | Maximum loudness and character |
| Gentle Glue | +3 dB | -0.5 dB | Subtle glue limiting |
| Streaming Safe | 0 dB | -1.0 dB | Extra headroom for lossy codecs |
| Broadcast | 0 dB | -3.0 dB | Broadcast-standard ceiling |
| Bus Limiter | +3 dB | -0.3 dB | Group bus protection |
| Fast Transient | +6 dB | -0.3 dB | Aggressive transient taming |
| Dual Mono | +3 dB | -0.3 dB | Independent L/R limiting |
| Remi Blaze Limit | +4 dB | -0.2 dB | Balanced loudness and transparency |

---

## 🐛 Bugs & Issues
Found a UI glitch, resize bug, or DAW-specific quirk? Open an issue on the **[Issues](https://github.com/RemiBlaze/Clampit/issues)** tab with your macOS or Windows version, DAW + version, and steps to reproduce.

---

## 📄 License & Credits
- **Plugin page:** [remiblaze.com/plugins/clampit/](https://remiblaze.com/plugins/clampit/).
- **Developer:** [Remi Blaze](https://remiblaze.com).
- **Framework:** [JUCE](https://juce.com).
- **License:** free under a proprietary [Freeware License](LICENSE) (see also our [terms](https://remiblaze.com/terms/)). Reverse-engineering, repackaging, binary redistribution, or reselling the compiled installer is strictly prohibited.

---

## Trademarks

All product names, company names, and logos mentioned herein are trademarks or registered trademarks of their respective owners. Any such references are used for descriptive or compatibility purposes only and do not imply affiliation with, endorsement by, or sponsorship from their owners.

VST is a trademark of Steinberg Media Technologies GmbH, registered in Europe and other countries.

Apple, macOS, Audio Units (AU), and Apple Silicon are trademarks of Apple Inc., registered in the U.S. and other countries.

AAX, Avid, and Pro Tools are trademarks or registered trademarks of Avid Technology, Inc. in the U.S. and other countries.

Microsoft and Windows are trademarks of the Microsoft group of companies.
