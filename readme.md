**START APPLICATION**
Review Bytegrad.

**NPM Necessary Libraries**
Sass works with NPM and Node. Libraries enable you to (1) write css with variables for palette, animations, and more. And (2) to optimize your css, (3) auto-prefix for edge case vendor browser support, and (4) compile a minified version of your css for production.

- Sass
- csso-cli
- postcss
- postcss-cli
- autoprefixer

**CSS SCRIPTS**
Look in package.json "scripts" for the pipeline that turns raw sass into production-ready css.

**RESET RELATIVE UNITS**
REM is relative to user setting. Default is 1 rem = 16px. Or 1 rem = 10px, if you scale your html default in step a below.

1. Add to style sheet: html {font-size: 100%; OR font-size: 62.5%}
2. Replace px fontsizes with rem units throughout
   - Translate specs like font-size 14px into .875rem.
   - Better yet, translate 14 into 1.4 rem, if you change to 62.5.
3. Replace px layouts with rem units throughout.
   - Translate specs like width 1280px into 77.5rem.

**MEDIA QUERIES**
Use the em unit. 1 em is 1 rem is browser font size (usually 16px or 10px if you use html font-size: 62.5%). There's a bug in Safari, so we use em here.

**CONVERSION**
You must use rems/ems. Do it manually in process, convert mathematically afterward, or convert with an npm package during build.
