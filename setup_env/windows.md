# Setup React Developping Environment on Windows

## Install Node.js

The first step is to download the Node.js installer for Windows. 
Let’s download [the Long Term Support (LTS) version](https://nodejs.org/en/download/) for Windows and choose the 64-bit version.

Followings are the command in windows cmd prompt. 

Press Win+R to open Run window. Type cmd in Run window then press Enter. In the cmd window, type the following commands. Note replace msi file with your downloaded file.

```bash
cd %USERPROFILE%/Downloads
dir *.msi
start node-v1x.xx.x-x64.msi
```

After installation is done, type the command to verify node.js version.

```bash
node --version
```
