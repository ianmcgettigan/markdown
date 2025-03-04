# markdown
Convert `.md` files to `.pdf` automatically and continuously on file save using Skim pdf viewer (for me, but may be useful for others, too).

1. Add the following to your vimrc (go to vim and run `:edit $MYVIMRC`):
  ```bash
  autocmd BufWritePost *.md silent !pandoc % -o %:r.pdf
  ```

