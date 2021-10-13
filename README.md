# Dark Mode for PDFs on OSX with Zathura

Mac's Preview app does not enable dark mode for PDF's. You can get that with the open source [Zathura](https://git.pwmt.org/pwmt/zathura).

Follow the [homebrew instructions](https://github.com/zegervdv/homebrew-zathura) to install with `homebrew`. 

You have two choices for the PDF engine: `poppler` and `mupdf`. While `mupdf` is supposed to be faster, I could only get it to work with `poppler`. I used the `--HEAD` options for `girara` and `zathura`.

After install and directory configuration (the `mkdir` and `ln -s` commands in the linked homebrew instructions), do:

```
mkdir ~/.config/zathura
cd ~/.config/zathura
touch zathurarc
```

Then open your `~/.config/zathura/zathurarc` file with a text editor and add the following lines.

```
set selection-clipboard clipboard
set recolor true
set recolor-darkcolor "#dcdccc"
set recolor-lightcolor "#1f1f1f"
```

The first line will enable the clipboard to work while the remaining lines perform the darkmode inversion.

`ctrl + cmd + r` switches from light to dark mode.

These [keyboard shortcuts](https://defkey.com/zathura-shortcuts) are helpful.
