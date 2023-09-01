---
title: Creating Bundled Installers for Client and Studio
description: A step-by-step guide to simplify the mass installation of the Roblox Client and Studio.
---

If you are part of an organization—such as a school or summer camp—that needs to install the Roblox Client or Studio on multiple computers, this guide is for you. While it is possible to individually install Roblox on each machine, doing so can be time-consuming. As a solution, we offer a way to create a bundled installer, which is a traditional executable file that can be easily deployed to multiple computers using software deployment and imaging tools. 

To help in this process, you can create your own bundled installer, giving you a traditional executable that can be installed on multiple computers. This can then be used in software deployment and imaging tools.

## Creating the Bundler

The following instructions are applicable to **Windows** computers.

1. **Download and Install Studio**: Navigate to <a href="https://www.roblox.com/create">Roblox Studio</a> and follow the on-screen instructions to install Studio on your computer.
2. Open the Command Prompt: Click the Windows Start icon, type `CMD` in the search bar, and click on the Command Prompt application.

   <img src="../../assets/education/legacy/showCommandPrompt.png" />

3. Find the installation of Roblox on your computer. You need the executable of what you'll be creating a bundle for. This will typically be in:

   `C:\Users\userName\AppData\Local\Roblox\Versions`

   <img src="../../assets/education/legacy/showVersions.png" />

   <Alert severity="info">
       If you see multiple folders, one will contain RobloxStudio.exe and another will contain RobloxPlayerLauncher.exe. Choose the folder according to the installer you want to create.
   </Alert>

4. In the Command Prompt, go to the location of the Roblox executable to use by
   typing `cd`, then the file path. and then <kbd>Enter</kbd>. For example:

   `cd C:\Users\userName\AppData\Local\Roblox\Versions\version-6d02431b656044a6`

5. Depending on the installer you want to create, type the file name, followed by -bundle, like below, and press <kbd>Enter</kbd>.

   ```bash
   RobloxStudioLauncherBeta.exe -bundle
   RobloxPlayerLauncher.exe -bundle
   ```

6. Let the bundler work until it closes.This will create a bundled installer in the same folder as the Roblox executable with a file name such as: `RobloxStudioLauncherBeta_version-6d02431b656044a6.exe`.

   <img src="../../assets/education/legacy/creatingBundler.png" />
