# TheFrequencyMan

This repository contains automation for building the **TheFrequencyMan** audio plugin using JUCE and Xcode. The workflow downloads JUCE, incorporates the plugin sources, generates an Xcode project, compiles a VST3 binary and packages the result.

## Build workflow
The `.github/workflows/build.yml` workflow performs these steps:

1. Check out the repository.
2. Download JUCE 5.4.7.
3. Copy the plugin source into the JUCE example structure.
4. Generate an Xcode project with Projucer.
5. Build in Release mode using Xcode.
6. Package the resulting `.vst3` file into a zip archive.
7. Upload the archive as a workflow artifact.

## Triggering the GitHub Action
The build is started manually from the **Actions** tab by selecting **Run workflow**.
