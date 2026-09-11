# GitHub Actions build instructions

This repository includes `.github/workflows/build.yml`.

## Build without installing Visual Studio

1. Create a new GitHub repository (private is fine).
2. Upload the **contents** of this folder to the repository root. Do not upload the outer ZIP as one file.
3. Commit the files to the `main` branch.
4. Open the repository's **Actions** tab.
5. Open **Build RLProfilePictures** and wait for the run to finish.
6. Open the successful run and download the **RLProfilePictures-DLL** artifact.
7. Extract the artifact. It contains `RLProfilePictures.dll`.
8. Back up your current working DLL before replacing it.

The workflow uses a Windows runner, downloads the BakkesMod SDK, installs the project's `vcpkg.json` dependency, builds `Release|x64`, and uploads only the resulting DLL.

If the build fails, download/copy the Actions error log and send it back for diagnosis.
