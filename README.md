# BlitzitOnLinux
A guide with information of how to run [Blitzit](https://www.blitzit.app/) app on GNU/Linux 🐧.

## Before start
* This method has been initially tested in Debian, other distros shoudn't have problems running Blitzit since the method isn't Debian-exclusive.
* You need to download the Blitzit app (*.exe win file) in the official website | [Donwload Blitzit for Desktop](https://www.blitzit.app/download-blitzit)
* Practically, we will be running Blitzit app through wine via Lutris. So, let's go!


## 1. Install winetricks
winetricks can be installed running a command in the terminal, generally there's no need to set-up extra repositories.

* For **Debian|Ubuntu** Linux-based distros:

```bash
sudo apt install winetricks
```
* For **Fedora** Linux-based distros:

```bash
sudo dnf install winetricks
```

* For **Arch** Linux-based distros:

```bash
sudo pacman -Sy winetricks
```

## 2. Install Lutris
The best and recommended option is the [Flatpack Lutris](https://flathub.org/en/apps/net.lutris.Lutris) version. However, you can download it from the Lutris official downloads page (see below at links of interest).

Once installed Lutris, at first-time open you'll see something like this. Don't worry, that are some auto-managed dependencies just installing.


## 3. Installing Blitzit with Lutris   
1. Clic on the plus ``+`` icon on the top left corner of the window, then press ``Install a Windows game from an executable``
2. Give a name to the app, leave the *Installer preset* field as ``Windows 10 64-bit (Default)``, and if you want to, change the *Locale* field with your preference language. Then press the ``Install`` button.
3. Press ``Install`` again on *wine Setup File* button.
4. Select or create a file path where the app will be installed, for example: ``/home/$USER/Blitzit``. Uncheck ``Create a desktop shortcut``, this won't be useful.
5. Press the ``⋮`` three dots button and select the ``.exe`` Blitzit setup file you have downloaded. Then press ``Install``
6. At this point, a Blitzit window will be appearing on your screen, go on and complete the login process. This will finalize the installation of the necessary files.
  > [!IMPORTANT]
  > The files are ready but Blitzit is not executable yet. Don't worry, just a few steps remaining.
7. Close the Blitzit app, back in the terminal press the ``Abort`` button, then uncheck ``Remove game files`` and press ``Yes`` button.

## 4. Setting up the executable Blitzit app in Lutris
1. Back in Lutris, clic on the plus ``+`` icon on the top left corner of the window, then press ``Add locally installed game``.
2. In ``Game info`` tab:
   * Set the name of the app.
   * Set ``Wine (Runs Windows games)`` in the *Runner* field.
3. In ``Game options`` tab:
   * In the *Executable* field press the ``⋮`` three dots button and select the file in the path ``/home/$USER/Blitzit/drive_c/users/$USER/AppData/Local/Programs/blitzit/Blitzit.exe``
   * In the *Working Directory* field press the ``⋮`` three dots button and select the installation directory  ``/home/$USER/Blitzit``
  > [!NOTE]
  > The ``/home/$USER/Blitzit`` directory is the example used in this guide, if your directory is different use it.
4. In ``Runner options`` tab make sure the ``Enable DXVK`` and ``Enable VKD3D`` are enabled (to be redundant).
5. Clic on ``Save`` button.
6. Press ``Play``.

That's it! You have the Blitzit app ready-to-go. Congratulations! 🎉

## Creating Desktop and Application Menu Shortcuts
To create desktop and application menu shortcuts for Blitzit, simply open Lutris and:
* Right click in the Blitzit app you have installed, then select ``Create desktop shortcut``.
* Right click in the Blitzit app you have installed, then select ``Create application menu shortcut``.

As you noticed, there is no icon in the Blitzit shortcuts, so follow this steps:
1. Right click in the Blitzit app in Lutris and select ``Configure``.
2. You will see the Lutris icon in the *Game info* tab, click on it to ``Set custom icon``.
3. The Blitzit icon is allocated in the path ``/home/$USER/Blitzit/drive_c/users/$USER/AppData/Local/Programs/blitzit/resources/assets/tray/icon.png`` (yeah, too long directory).
4. Click on ``Save`` button.

Finally, you have created the shortcuts and set correctly the icon on it.

Note: The ``Blitzit.lnk`` file in desktop is unneecssary, just delete it.

# Extra info, tips and troubleshooting.
* If you are having glitching problems, consider changing *Wayland* to *X11* graphic interface.
* Surprisingly, all features are functional at the time of writing this guide.
* I have not been able to update the app since the opportunity has not yet been given. However, I am very sure that if a new update is released, it will be done automatically considering how the app works on Windows. When this happens, this guide will be updated with that information.

# Links of interest
* [Blitzit App](https://www.blitzit.app/) official page
* [winetricks](https://github.com/Winetricks/winetricks) official GitHub page
* [Lutris](https://lutris.net/downloads) official downloads page

# Disclaimer
I'm not affiliated with Blitzit and this guide has been made solely for informational and non-profit purposes.
