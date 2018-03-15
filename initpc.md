* [Chrome dev](https://www.google.com/chrome/?hl=zh-CN&extra=devchannel)
* [Git](https://git-scm.com/downloads)
* [NVM](https://github.com/creationix/nvm) [nvm-win](https://github.com/coreybutler/nvm-windows)
* [JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
* [360 Driver.exe](https://dl.360safe.com/drvmgr/360DrvMgrInstaller_beta.exe)
* [lantern-win.exe](https://raw.githubusercontent.com/getlantern/lantern-binaries/master/lantern-installer.exe)
  [lantern-mac.dmg](https://raw.githubusercontent.com/getlantern/lantern-binaries/master/lantern-installer.dmg)
* [TIM](http://office.qq.com/download.html)
* [WeChat](https://weixin.qq.com)
* [MiCloud](https://i.mi.com/static2?filename=MicloudWebStatic/res/home/mi-lab.htm&locale=zh_CN#3)
* [GitBook](http://downloads.editor.gitbook.com)
* [LLVM-Clang](http://releases.llvm.org/download.html)
* Ubuntu on Windows in Microsoft Store
## Node.JS
```bash
# Windows
nvm node_mirror https://npm.taobao.org/mirrors/node/
nvm npm_mirror https://npm.taobao.org/mirrors/npm/
nvm install latest
npm install --global --production windows-build-tools
# Ubuntu
uname -sr # 查看内核
cat /etc/issue # 查看发行版本
sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
sudo vi /etc/apt/sources.list

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-security main restricted universe multiverse

deb https://mirrors.aliyun.com/ubuntu/ xenial main restricted
deb https://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted
deb https://mirrors.aliyun.com/ubuntu/ xenial universe
deb https://mirrors.aliyun.com/ubuntu/ xenial-updates universe
deb https://mirrors.aliyun.com/ubuntu/ xenial multiverse
deb https://mirrors.aliyun.com/ubuntu/ xenial-updates multiverse
deb https://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
deb https://mirrors.aliyun.com/ubuntu/ xenial-security main restricted
deb https://mirrors.aliyun.com/ubuntu/ xenial-security universe
deb https://mirrors.aliyun.com/ubuntu/ xenial-security multiverse

deb https://mirrors.163.com/ubuntu/ xenial main restricted universe multiverse
deb https://mirrors.163.com/ubuntu/ xenial-updates main restricted universe multiverse
deb https://mirrors.163.com/ubuntu/ xenial-backports main restricted universe multiverse
deb https://mirrors.163.com/ubuntu/ xenial-security main restricted universe multiverse
# 帮助文档：https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/
# 帮助文档：https://opsx.alibaba.com/mirror

sudo apt-get update
sudo apt-get upgrade
sudo do-release-upgrade
echo 'export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node' >> ~/.bashrc
nvm install node

npm config set registry https://registry.npm.taobao.org
npm i -g yarn
yarn global bin的输出加入path环境变量
yarn global add yarn
npm uninstall -g yarn
yarn global add cnpm
yarn global add node-gyp
```
## Rust Lang
* 配置 rustup 中国镜像源
```bash
# 环境变量
export RUSTUP_DIST_SERVER=https://mirrors.ustc.edu.cn/rust-static
export RUSTUP_UPDATE_ROOT=https://mirrors.ustc.edu.cn/rust-static/rustup
```
* [rustup.exe](https://win.rustup.rs/)
* rustup.sh `curl https://sh.rustup.rs -sSf | sh`
* 配置 Rust Crates 镜像
```
vi $HOME/.cargo/config

[source.crates-io]
registry = "https://github.com/rust-lang/crates.io-index"
replace-with = 'ustc'
[source.ustc]
registry = "git://mirrors.ustc.edu.cn/crates.io-index"
```
* 添加 nightly
```
rustup install nightly
rustup default nightly
rustup update
rustup show
```