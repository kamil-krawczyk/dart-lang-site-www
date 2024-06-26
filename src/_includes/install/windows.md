
### Install using Chocolatey {:.no_toc}

To install the Dart SDK, use [Chocolatey][Chocolatey].
Chocolatey requires [elevated permissions].

1. Install Chocolatey.

1. Launch [PowerShell][] with elevated permissions.

   ```ps
   PS C:\> choco install dart-sdk
   ```

### Change default install path {:.no_toc}

By default, Chocolatey installs the SDK at `C:\tools\dart-sdk`.
To change that location, set the [`ChocolateyToolsLocation`][]
environment variable to your desired installation directory.

### Verify your PATH includes Dart {:.no_toc}

Verify you can run Dart.

```ps
PS C:\> dart --version
Dart SDK version: 3.2.4 (stable) (Thu Dec 21 19:13:53 2023 +0000) on "win_x64"
```

If your development machine doesn't return a Dart version,
add the SDK location to your PATH:

1. In the Windows search box, type `env`.
2. Click **Edit the system environment variables**.
3. Click **Environment Variables...**.
4. In the user variable section, select **Path** and click **Edit...**.
5. Click **New**, and enter the path to the `dart-sdk` directory.
6. In each window that you just opened,
   click **Apply** or **OK** to dismiss it and apply the path change.

### Upgrade using Chocolatey {:.no_toc}

To upgrade the Dart SDK, use the following command.

```ps
PS C:\> choco upgrade dart-sdk
```

### Uninstall using Chocolatey {:.no_toc}

To uninstall the Dart SDK, perform the following steps.

1. Launch [PowerShell][] with elevated permissions.

1. Use the following command.

   ```ps
   PS C:\> choco uninstall dart-sdk
   ```

1. Remove the Dart configuration files from your home directory.

   ```ps
   PS C:\> Remove-Item -Recurse -Force ^
        -Path $env:LOCALAPPDATA\.dartServer,$env:APPDATA\.dart,$env:APPDATA\.dart-tool
   ```

[elevated permissions]: https://www.thewindowsclub.com/elevated-privileges-windows
[PowerShell]: https://www.thewindowsclub.com/how-to-open-an-elevated-powershell-prompt-in-windows-10
[Chocolatey]: https://chocolatey.org
[`ChocolateyToolsLocation`]: https://stackoverflow.com/questions/19752533/how-do-i-set-chocolatey-to-install-applications-onto-another-drive/68314437#68314437
