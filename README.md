> [!NOTE]
> This is a fork of the original [corvinusmetropolis theme](https://github.com/magyarkuti/corvinusmetropolis) made by professor Magyarkuti Gyula. This repo is mainly for personal use with the university's new design elemnent, and some other university designs as well, but feel free to use it if you would like.

This extension is built on top of the **Metropolis** theme for **beamer** in **LaTeX**. For further documentation on the metropolis theme, refer to 
<https://www.tug.org/texlive//Contents/live/texmf-dist/doc/latex/beamertheme-metropolis/metropolistheme.pdf>

----

# Corvinus LaTeX Presentation Theme

This is an unofficial presentation theme created for professors and students of Corvinus University Budapest and for friends and colleges of other hungarian universities. The theme is a custom design built on top of metropolis theme in beamer.  

I am currently working on a bachelor's/master's thesis template as well, feel free to contribute!

## Usage

You can download the latest `.zip` version from the releases page, or you can clone the whole repo as well.  
For the main presentation, edit the `template.tex` file. You can find more options (fonts, color, logos)inside!

## Compilation

Because of local fonts in the `.fonts/` folder, you need to compile the document using `xelatex`. If you are using vim to edit your documents with the [VimTeX](https://github.com/lervag/vimtex) plugin, autocompilation will work with `latexmk`.

## Features

### Citations built-in

The template has biblatex baked in, with APA citations style configured (BCE standard style). To use biblatex, uncomment the corresponding lines in the `.tex` preamble! For managing `.bib` files, I reccomend using Zotero or JabRef.

## Vimtex configuration

To edit LaTeX files, you can use your favorite TeX editor (TeXstudio. Texmaker, ...), but i would recommend using NeoVim with the vimtex plugin installed. For starting out, I attached my personal configuration!  

Vimtex configuration example with lazy.nvim:
```lua
{
  'lervag/vimtex',
  lazy = false, -- we don't want to lazy load VimTeX
  -- tag = "v2.15", -- uncomment to pin to a specific release
  init = function()
    -- VimTeX configuration goes here, e.g.
    vim.g.vimtex_view_method = 'zathura'
    vim.g.vimtex_view_forward_search_on_start = false
    vim.g.vimtex_compiler_latexmk = {
      aux_dir = '/home/user/.texfiles/', -- auxilarry texfile location
      -- out_dir = '/home/user/.texfiles/' -- output location of pdf files
    }
  end,
}
```
