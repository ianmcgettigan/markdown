# markdown
Convert `.md` files to `.pdf` automatically and continuously on file save using Skim pdf viewer (for me, but may be useful for others, too).

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

