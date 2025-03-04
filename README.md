# Convert markdown to pdf automatically and continuously using Skim and Pandoc.
Convert `.md` files to `.pdf` automatically and continuously on file save using Skim pdf viewer (for me, but may be useful for others, too).

Inspired by the way Vim-TeX automatically compiles `.tex` files and updates `.pdf` on save. This is much simpler as it only uses one
command in the background, but it saves the hassle of manually running `pandoc file.md -o file.pdf` every time, and refreshing the pdf
viewer every time.

1. Add the following to your vimrc (go to vim and run `:edit $MYVIMRC`):
  ```bash
  autocmd BufWritePost *.md silent !pandoc % -o %:r.pdf
  ```
2. Go to Skim settings
  - Go to Sync tab
  - Set the preset to `Custom`
  - Enter a dummy command; e.g., `usr/bin/true`
  - Enable the option "Check for file changes" and "Reload automatically"

You're now good to go. The first time you try this Skim may alert you with a popup. Just select "Auto" and it won't annoy you again.

