# N I X S T

## Dependencies

```
# Void
xbps-install libXft-devel libX11-devel harfbuzz-devel libXext-devel libXrender-devel libXinerama-devel
# Debian (and ubuntu probably)
apt install build-essential libxft-dev libharfbuzz-dev
# Nix
nix develop github:siduck/st
(most of these are already installed on Arch based distros)
# Install font-symbola and libXft-bgra
```

## Install

```
git clone https://github.com/nixenos/nixst.git
cd nixst
sudo make install
```
## Patches:

- Ligatures
- sixel (check sixel branch)
- scrollback
- Clipboard
- Alpha(Transparency)
- Boxdraw
- patch_column ( doesnt cut text while resizing)
- font2
- right click paste
- st desktop entry
- newterm
- anygeometry
- xresources
- sync patch ( Better draw timing to reduce flicker/tearing and improve animation smoothness )
- live reload ( change colors/fonts on the fly )
  and more...
    <br>

    ## Xresources live-reload

    ```
    # make an alias for this command
    alias reload-st="xrdb merge ~/.Xresources && kill -USR1 $(pidof st)"
    ```

    ## Default Keybindings<br>

    <pre>
    ctrl + shift + c        Copy  <br>
    ctrl + shift + v        Paste <br>
    right click on the terminal ( will paste the copied thing )

    (Zoom)
    alt  + comma            Zoom in <br>
    alt  + .                Zoom out <br>
    alt  + g                Reset Zoom<br>

    (Transparency)
    alt  + s                Increase Transparency<br>
    alt  + a                Decrease Transparency<br>
    alt  + m                Reset Transparency<br>

    alt + k                 scroll down
    alt + j                 scroll up

    mod + shift + enter    open a new terminal with same cwd ( current working directory )
    </pre>

    you can change all of these in config.h
    <br>

    # Credits

    - [live-reload](https://github.com/nimaipatel/st)
    - [patch_column](https://github.com/nimaipatel/st/blob/all/patches/7672445bab01cb4e861651dc540566ac22e25812.diff)
    - [siduck - base of this st distribution](https://github.com/siduck/st)
