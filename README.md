## 下载zsh/git

```bash
sudo apt update
sudo apt install zsh git
```
## 安装oh-my-zsh

```bash
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
## 设置zsh为默认

```bash
chsh -s /bin/zsh
```
## 查看oh-my-zsh自带的主题

```bash
cd ~/.oh-my-zsh/themes && ls
```
如果更换`oh-my-zsh`自带主题，需修改`ZSH_THEME=XXX`，例如`ZSH_THEME="cloud"`
## 下载更换 Dracula 主题

> ​		[Dracula->zsh](https://draculatheme.com/zsh)

```bash
git clone https://github.com/dracula/zsh.git
```
## 移动文件到zsh配置

```bash
cp zsh/dracula.zsh-theme ~/.oh-my-zsh/themes
cp -r zsh/lib/ ~/.oh-my-zsh/themes
```
## 更改zsh主题为 dracula

```bash
nano ~/.zshrc
```

更改内容`ZSH_THEME="dracula”`


## 更新配置
```bash
source ~/.zshrc
```

## 更换 powerlevel10k 主题

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
## 更改zsh主题为 powerlevel10k

```bash
nano ~/.zshrc
```

更改内容`ZSH_THEME="powerlevel10k"`

## 更新配置
```bash
source ~/.zshrc
```
⚠️注意：一定要设置好终端字体，否则会出现图标无法正常显示的现象，可以下载powerlevel10k官网推荐的四个字体：`https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#meslo-nerd-font-patched-for-powerlevel10k`


## 命令补全

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
```
nano ~/.zshrc
```

## 更改内容

```bash
plugins=(
	git
	zsh-autosuggestions
)
```
## 更新配置

```bash
source ~/.zshrc
```


## 代码高亮

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
```
nano ~/.zshrc
```

## 更改内容

```bash
plugins=(
	git
	zsh-autosuggestions
	zsh-syntax-highlighting
)
```

## 更新配置

```bash
source ~/.zshrc
```
