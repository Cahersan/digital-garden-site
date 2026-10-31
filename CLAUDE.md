# Site repo

Quartz v4 site for the digital garden. `README.md` documents the two-repo structure, deploy pipeline, GitHub secrets and maintenance; read it before changing any of those.

## Rules

- `content` is a symlink to `../notes`, a separate repo. Never edit, create or delete notes from here.
- Never add `content` to `.gitignore`: Quartz skips gitignored files. It is excluded via `.git/info/exclude`.
- Put customizations in `quartz.config.ts`, `quartz.layout.ts` or `quartz/styles/custom.scss`. Edit other files under `quartz/` only when there is no other way, since they conflict with upstream updates.
- Record every change relative to upstream Quartz in the README's Customization table.

## Commands

Node comes from nvm: run `source ~/.nvm/nvm.sh` first in non-interactive shells.

- `npx quartz build`: build into `public/`.
- `npx quartz build --serve`: local preview at http://localhost:8080.
