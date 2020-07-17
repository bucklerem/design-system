# Plan

A basic way to track what needs to be done and keep it close to source code.

## Goals

- Provide public documentation about Project U-Turn and getting started information for anyone to be able to start using what's available.
- Clarify the differences between Project U-Turn and React distributions.

## TODO

### Build / Lerna

- [ ] BUILD-1: BUG -- Setup start/build script to avoid a race condition. @umich-lib/components must built before @umich-lib/docs, for example, otherwise it will error. The present workaround is to build at least once then start. We may want to build CSS -> Components -> DOCS, but this needs further investigation.

### components

- [ ] COMP-1: Figure out a component documentation strategy and then configure @umich-lib/components docs-json output ([auto-generated JSON documentation](https://stenciljs.com/docs/docs-json)). Then distribute that JSON, so that it can be consumed, by @umich-lib/docs for example.
- [ ] COMP-2: Consider if Storybook should live within the @umich-lib/components package and not at the root.

### css

- [ ] CSS-1: Setup Gulp watch on `npm start` so that development doesn't required a re-start.

### icons

- [ ] ICONS-1: Figure out a way to make the icon component only load what it needs. Investigate this and recommend improvements. Related article: https://paulcpederson.com/articles/stencil-icons/

### docs

- [x] DOCS-1: Import @umich-lib/components doc JSON.
- [x] DOCS-2: Generate component pages.
- [x] DOCS-3: Create introduction / getting started page.
- [x] DOCS-4: Add code highlighting.
- [ ] DOCS-5: Add code highlighting per line.
- [x] DOCS-6: Figure out a FOUC solution.
- [ ] DOCS-7: Add favicon.
- [x] DOCS-8: Add design token related documentation, but likely a lot to consider about to what expose and maintain. Probably for now custom variables spacings, colors, and utilities. https://piccalil.li/cube-css/
- [ ] DOCS-9: Add browser compatability and make sure the DS meets our targets.
- [ ] DOCS-10: Add copy command for packages relied on so that they are used locally. This will make development of all the packages possible. Inspired by: https://www.duetds.com/using-components/#usage-with-basic-html

- [ ] DOCS-N: Usability test the docs with an LIT developer.