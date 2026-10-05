# specVoice 2.0

Expressive text-to-speech for Windows, built on the **Specology v0.4** framework.

- **src/SpecVoice.Core**: the rendering library (net8.0). It covers Edge neural client, planner (emotion, slang, tags, melody), DSP, effects, voice catalog, accents, learner and external engines.
- **src/SpecVoice.App**: the WinForms app (net8.0-windows).
- **tests/SpecVoice.Tests**: 37 xunit tests.
- **libs/SpecCore**: Specology v0.4, unmodified.
- **docs**: [User manual](docs/USER_MANUAL.md) · [Research](docs/RESEARCH.md) · [100 improvements reviewed](docs/IMPROVEMENTS.md) · [Store listing](docs/STORE_DESCRIPTION.md)

## Build
```
dotnet build SpecVoice.sln -c Release
dotnet test tests/SpecVoice.Tests
```
Or open `SpecVoice.sln` in Visual Studio 2022 and run **SpecVoice.App**.

## Library quick start
```csharp
var s = new SpecVoice.Core.VoiceSettings { VoiceShortName = "en-US-AvaNeural" };
await SpecVoice.Core.Tts.SaveWavAsync("[excited] It works!", "out.wav", s);
```

Licences: MP3Sharp (LGPL-3.0, NuGet), NAudio (MIT), System.Speech (MIT).
