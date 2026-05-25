> [!NOTE]
> This is a fork of the original [corvinusmetropolis theme](https://github.com/magyarkuti/corvinusmetropolis) made by professor Magyarkuti Gyula. This repo is mainly for personal use with the university's new design elemnent, and some other university designs as well, but feel free to use it if you would like.

This extension is built on top of the **Metropolis** theme for **beamer** in **LaTeX**. For further documentation on the metropolis theme, refer to 
<https://www.tug.org/texlive//Contents/live/texmf-dist/doc/latex/beamertheme-metropolis/metropolistheme.pdf>

----

WIP

# Corvinus presentation theme

This is an unofficial presentation theme created for professors and students of Corvinus University Budapest and for friends and colleges of other hungarian universities. The theme is a custom design built on top of metropolis theme in beamer.

I am currently working on a bachelor's/master's thesis template as well, feel free to contribute!

## Usage

## Compilation

Because of local fonts in teh `.fonts` folder, you need to compile the document using `xelatex`. If you are using vim to edit your documents with the [vimtex plugin](https://github.com/lervag/vimtex), autocompilation will work with `latexmk`.
## Features

### Reproducibility

### Citations built-in

## Vimtex configuration

Vimtex configuration example:
```lua
require('lazy').setup({
    {
        'lervag/vimtex',
        lazy = false, -- we don't want to lazy load VimTeX
        -- tag = "v2.15", -- uncomment to pin to a specific release
        init = function()
          -- VimTeX configuration goes here, e.g.
          vim.g.vimtex_view_method = 'zathura'
          vim.g.vimtex_view_forward_search_on_start = false
          vim.g.vimtex_compiler_latexmk = {
            aux_dir = '/home/user_name/.texfiles/', -- auxilarry texfile location
            -- out_dir = '/home/user_name/.texfiles/' -- output location of pdf files
          }
        end,
    }
})
```
