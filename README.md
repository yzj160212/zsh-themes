# 设置oh-my-zsh主题

## 下载zsh/git(debian系统)

```bash
sudo apt update
sudo apt install zsh git
```
## brew下载zsh/git/wget(Mac系统)

```bash
brew install wget git zsh
```
-  安装oh-my-zsh

```bash
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
-  设置zsh为默认

```bash
chsh -s /bin/zsh
```
-  查看oh-my-zsh自带的主题

```bash
cd ~/.oh-my-zsh/themes && ls
```
如果更换`oh-my-zsh`自带主题，需修改`ZSH_THEME=XXX`，例如`ZSH_THEME="cloud"`

## 更换 Agnoster 主题

```bash
nano ~/.zshrc
```

更改内容`ZSH_THEME="agnoster"`

-  更新配置

```bash
source ~/.zshrc
```
## 安装 Powerline 字体

-  `为了展示 Agnoster 主题提示符里的三角形，需要 Powerline 字体库的支持`
-  克隆 Powerline 字体仓库
```bash
git clone https://github.com/powerline/fonts.git
```
-  安装字体

```bash
cd fonts
./install.sh
```
-  清理(安装完字体以后,删除字体文件夹)

```bash
cd ..
rm -rf fonts
```

## 更换 Dracula 主题

> ​		[Dracula->zsh](https://draculatheme.com/zsh)

```bash
git clone https://github.com/dracula/zsh.git
```
-  移动文件到zsh配置

```bash
cp zsh/dracula.zsh-theme ~/.oh-my-zsh/themes
cp -r zsh/lib/ ~/.oh-my-zsh/themes
```
-  更改zsh主题为 dracula

```bash
nano ~/.zshrc
```

更改内容`ZSH_THEME="dracula”`


-  更新配置
```bash
source ~/.zshrc
```

## 更换 powerlevel10k 主题

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
-  更改zsh主题为 powerlevel10k

```bash
nano ~/.zshrc
```

更改内容`ZSH_THEME="powerlevel10k/powerlevel10k"`

-  更新配置

```bash
source ~/.zshrc
```

⚠️注意：一定要设置好终端字体，否则会出现图标无法正常显示的现象，可以下载powerlevel10k官网推荐的四个字体：`https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#meslo-nerd-font-patched-for-powerlevel10k`


## 安装插件
-  命令补全

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

-  代码高亮

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

-  打开nano编辑器

```bash
nano ~/.zshrc
```

-  修改内容

```bash
plugins=(
	git
	zsh-autosuggestions
	zsh-syntax-highlighting
)
```

-  更新配置

```bash
source ~/.zshrc
```

## 完事🐒
