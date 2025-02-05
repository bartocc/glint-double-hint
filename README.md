# Readme

Demo VSCode project to demonstrate the glint double hint issue discussed here:
https://discord.com/channels/480462759797063690/1334122360831475772

## Steps to reproduce

- `git clone https://github.com/bartocc/glint-double-hint.git`
- `cd glint-double-hint`
- `npm install`
- `code --install-extension typed-ember.glint-vscode`

### Single hint repro

- `code .`
- `code web/index.gts`
- hover over `Foo`
- you should see a single hint

### Double hint repro

- `open glint-double-hint.code-workspace`
- `code web/index.gts`
- hover over `Foo`
- you should see a double hint

You can now fix the double hint with the following steps

- `code glint-double-hint.code-workspace`
- replace the `folders` key with `"folders": [{ "path": "web" }],`
- `code web/index.gts`
- hover over `Foo`
- you should see a single hint
