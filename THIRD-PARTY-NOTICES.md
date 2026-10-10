# RVC Dynamic F0 redistribution notices

This release is a collection of independently licensed components, not a claim that every bundled component is MIT-licensed. Preserve the original notices and comply with the applicable component licenses when redistributing it.

## Application and model assets

- **RVC application**: derived from [RVC-Project/Retrieval-based-Voice-Conversion-WebUI](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI), including the original MIT license and copyright notices. The GPU archive contains the application source as a snapshot, not the private repository's Git history.
- **Dynamic F0 and launcher changes**: the release includes the modified application source and an optional source/notices archive containing the native launcher's C# source and build script. These sources can be studied and rebuilt without access to the development repository.
- **HuBERT and RMVPE checkpoints**: downloaded unchanged from [lj1995/VoiceConversionWebUI at the pinned revision](https://huggingface.co/lj1995/VoiceConversionWebUI/tree/e6d0c1a17da07c33557852f9dfa2bd44cc75737d). The [HuBERT model origin](https://huggingface.co/facebook/hubert-base-ls960) and [RMVPE reference implementation](https://github.com/Dream-High/RMVPE) carry their own notices; the RVC conversion/distribution is not a grant of rights to a purchased voice.
- **FCPE**: the checkpoint and package supplied by `torchfcpe==0.0.4` retain that package's MIT notice. None of these general inference assets is the user's purchased voice model.

## Bundled runtime and libraries

The extracted runtime retains package license files. This download repository also preserves the license/notice files extracted from the actual payload under `licenses/bundled/`; the source archive includes those copies for convenience.

- **Python 3.12.10, Tcl/Tk and inference dependencies**: retain their shipped licenses and notices. The exact installed versions are recorded in the GPU archive's `portable-dependencies.txt`, copied here as `DEPENDENCIES.txt`.
- **PyTorch 2.7.1+cu118 and torchaudio**: their license and third-party notice files are preserved, including notices for libraries supplied with their binary distributions. CUDA-related components remain under their respective NVIDIA terms rather than this repository's license.
- **Praat-Parselmouth 0.4.7**: distributed under GPLv3. Its exact version's source distribution, including Praat source, is included in the optional source/notices archive.
- **FreeSimpleGUI 5.1.1**: retains the original LGPL3-derived project notice and source distribution. The app's Tcl/Tk compatibility adjustment lives in the supplied app source and does not replace the library's license.
- **SoXR 1.1.0 / libsoxr**: retain the wrapper and library notices, including libsoxr's LGPL terms. The version-matched source distribution is supplied with its included libsoxr source.
- **SoundFile 0.14.0 / libsndfile 1.2.2**: retain their separate wrapper and native-library licenses. Both corresponding source archives are supplied.
- **Audioread 3.1.0**: its version-matched source distribution is supplied and the package's original license remains applicable.

## Native extractor

The launcher embeds unmodified `7z.exe` and `7z.dll` version 26.03. Their exact embedded [7-Zip distribution notice](licenses/LICENSE-7zip.txt) is reproduced here, and version-matched upstream source is supplied in the optional source archive; see [upstream 7-Zip](https://www.7-zip.org/license.txt).

The embedded files are used as external extraction tools. The launcher source and build recipe are included so recipients can rebuild the launcher with replacement extractor resources; there is no authenticity lock restricting modified rebuilds.

## Source availability

`RVC-Dynamic-F0-Licenses-and-Sources.zip` is a companion release asset containing the application source snapshot, launcher source/build recipe, the collected original notices, and upstream source distributions. `SOURCE-MANIFEST.json` records the original URLs and SHA-256 values of the collected upstream source artifacts.

These source and notice files are not needed to run the app, and users should still download only the three main app files for normal use. No paid voice model, personal device settings, access credentials or private Git history is included in this distribution.
