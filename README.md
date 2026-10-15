# TalkFlow releases

This public repository distributes **compiled TalkFlow installers and update packages**. Application source code remains in the private `MiMat82/Talkflow` repository.

TalkFlow is a Windows dictation app with local Danish, English and Mandarin recognition. It uses a small floating control, hold-to-talk and double-tap hands-free recording. Dictation runs locally; its separate updater checks this repository for published stable releases.

Download the [Windows Setup](https://github.com/MiMat82/Talkflow-release/releases/latest/download/MiMat82.TalkFlow-win-x64-Setup.exe) from the [latest release](https://github.com/MiMat82/Talkflow-release/releases/latest). Requires Windows 11 x64 and an AVX2-capable CPU.

Existing packaged installations: right-click the floating TalkFlow control, choose **Check for updates**, then **Update and restart**. The app also checks automatically while idle. No GitHub account is required. A raw development folder needs the one-time Setup installation before it can update itself.

**Novalon · Denmark · CVR 45642399**

## Maintainer release process

1. Commit and push tested source changes to the private source repository.
2. Open **Actions → Package TalkFlow → Run workflow** in this release repository and enter the next `major.minor.patch` version.
3. The workflow reads the private source using a dedicated **read-only deploy key**, tests and packages it with the pinned Velopack CLI, and creates a **draft release** containing installers, full/delta update packages and the release feed.
4. Review and test the draft's installer/update before publishing the release. Only a published, non-prerelease stable release becomes visible to clients.

The publishing token is this repository's short-lived `GITHUB_TOKEN`. No owner token is copied into an application or stored for CI publishing. `TALKFLOW_SOURCE_READ_KEY` grants only read access to the private source repository and is stored as an encrypted Actions secret. This workflow runs manually on trusted repository code, not on external pull requests.

Do not add source archives, models or binaries directly to Git history; distribute the generated application packages as release assets. The compiled application's third-party notices are included in each package. Public release files do not change the license or visibility of the private application source.
