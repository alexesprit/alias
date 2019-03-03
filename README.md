View and set command aliases in Windows.

## How to setup?
Just cd in `alias` dir and run `alias`. It will ask you for installation if neccessary.

By default aliases are stored in `%USERPROFILE%\Documents\Scripts\Aliases`. You can set the directory to store aliases by changing the environment variable called `%ALIASES_DIR%`.

## Managing aliases
Get the list of available aliases:
```cmd
> alias
apktool, gsh, gst
> alias -v
apktool = %SOFTWARE%\apktool\apktool.bat %*
gsh = git show $*
gst = git status --short --branch %*
```
Add an alias:
```cmd
> alias test=dir \b %*
Added test
```
Show the alias:
```cmd
> alias g
gsh, gst
> alias test
dir \b %*
```
Search for a text in alias commands:
```cmd
> alias -s apk
baksmali, smali
> alias -s apk -v
baksmali = %SOFTWARE%\apktool\apktool.bat d %*
smali = %SOFTWARE%\apktool\apktool.bat b %*
```
Remove the alias:
```cmd
> alias -d test
Removed test
```

## Environment variables
`alias` changes two variables:
1. `%ALIASES_DIR%`
Directory where aliases are stored.
2. `%PATH%`
Adds `%ALIASES_DIR%` to `%PATH%`.

## License

Licensed under [MIT License](LICENSE.md).