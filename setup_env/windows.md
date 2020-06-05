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

## Configure Node

Node.js uses npm to manage configuration. Use the default settings of node.js is a very common method. This section is optional if you use default settings. But if you are in your company intranet or if you are in some countries like china mainland, you'd better set the proxy and the repo url of npm. Follow the steps in this section.

### Set proxy and registry for npm
```bash
# Show the current npm variables
npm config list
# Change proxy 
npm config set proxy "http://your-proxy:port"
# Change registry to taobao
npm config set registry "https://registry.npm.taobao.org"
```

### Use alternated registry in argument of npm
```bash
# use alternated registry, cache and user config.
npm --registry=https://registry.npm.taobao.org \
  --cache=$HOME/.npm/.cache/cnpm \
  --disturl=https://npm.taobao.org/dist \
  --userconfig=$HOME/.cnpmrc
```

### Use env variable of npm
```bash
# npm using env variable
npm_config_registry=https://registry.npm.taobao.org npm
# npx is an internal tool of npm
npm_config_registry=https://registry.npm.taobao.org npx
```
