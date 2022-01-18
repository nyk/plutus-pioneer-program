# Project Setup Checklist

1. Make sure you have the plutus-apps project cloned on your local system.
2. Open the cabal.project file in plutus-pioneer-program in the correct code and week directories.
3. Search for the plutus-apps dependency in the cabal.project file.
4. Copy the git commit tag for the commit of plutus-apps version this project is built against.
5. Go to the plutus-apps clone and run `git checkout` with the commit tag you copied.
6. Rebuild plutus-apps by entering the `nix-shell` in the project root.
7. In the nix-shell, navigate to your weekly project directory and build the project with `cabal build`.
8. If you get an error about an outdated version of the package list, you might have to update it first with `cabal update`.

NOTE: It is important to make sure that your plutus-apps and project are using the same commit tag for the plutus-apps libraries. It is also important that you use a nix-shell opened from plutus-apps directory and navigate to your project root to build your project.
