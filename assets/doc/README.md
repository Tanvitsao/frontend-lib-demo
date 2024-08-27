## Build

Run `ng build merc-lib` to build the project. The build artifacts will be stored in the `dist/` directory.
ios: 每次 `npm run build`或 `npm run build:patch`後，請重新執行 `npm run build:schemas`，產生指令檔。
windows: 每次 `npm run build`或 `npm run build:patch`後，請重新執行 `npm run build:schemas`，產生指令檔，由於OS指令問題，robocopy不會自動重試，如檔案有複製成功且exit code 為 1，手動執行至成功Copy結束就可以了。

在 merc-lib 目錄下：
1. Run `npm run build` 打包 merc-lib，更新次版號
2. Run `npm run build:patch` 打包 merc-lib，更新修訂號
3. Run `npm run build:schemas` 打包 schematics 到 dist/merc-lib 目錄下，若 merc-lib 有更新，請先執行merc-lib 打包再執行 schematics 打包
4. Run `npm run build:release` 打包 merc-lib，更新次版號，並且釋出該版本號Tag及changelog。
5. Run `npm run build:release:patch` 打包 merc-lib，更新修訂號，並且釋出該版本號Tag及changelog及Readme。
6. Run `npm run pushtag` 推版本號到master。

## Publishing

After building your library with `ng build merc-lib`, go to the dist folder `cd dist/merc-lib` and run `npm publish`.

## Running unit tests

Run `ng test merc-lib` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
