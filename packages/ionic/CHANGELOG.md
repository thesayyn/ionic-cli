# Change Log

All notable changes to this project will be documented in this file.
See [Conventional Commits](https://conventionalcommits.org) for commit guidelines.

## [5.2.4](https://github.com/ionic-team/ionic-cli/compare/ionic@5.2.3...ionic@5.2.4) (2019-08-07)

**Note:** Version bump only for package ionic





## [5.2.3](https://github.com/ionic-team/ionic-cli/compare/ionic@5.2.2...ionic@5.2.3) (2019-07-15)

**Note:** Version bump only for package ionic





## [5.2.2](https://github.com/ionic-team/ionic-cli/compare/ionic@5.2.1...ionic@5.2.2) (2019-07-09)


### Bug Fixes

* **cordova:** revert to `--no-connect` as default ([e4368a8](https://github.com/ionic-team/ionic-cli/commit/e4368a8))
* **deploy:** support custom Capacitor build directory ([#4065](https://github.com/ionic-team/ionic-cli/issues/4065)) ([6146296](https://github.com/ionic-team/ionic-cli/commit/6146296))





## [5.2.1](https://github.com/ionic-team/ionic-cli/compare/ionic@5.2.0...ionic@5.2.1) (2019-06-28)

* **deploy:** fix bug with `ionic deploy configure` in CI ([7774dfe](https://github.com/ionic-team/ionic-cli/commit/7774dfe))





# [5.2.0](https://github.com/ionic-team/ionic-cli/compare/ionic@5.1.1...ionic@5.2.0) (2019-06-26)


### Bug Fixes

* **capacitor:** save Capacitor CLI in dev deps ([dd2fd86](https://github.com/ionic-team/ionic-cli/commit/dd2fd86))
* **cordova:** rely on package.json for plugins/platforms ([286917f](https://github.com/ionic-team/ionic-cli/commit/286917f))


### Features

* **angular:** pass `--verbose` to Angular CLI ([cf611ed](https://github.com/ionic-team/ionic-cli/commit/cf611ed))
* **angular:** pass `--verbose` to Angular CLI for serve ([3f9e859](https://github.com/ionic-team/ionic-cli/commit/3f9e859))
* **repair:** add `--cordova` flag for only repairing Cordova ([1055b49](https://github.com/ionic-team/ionic-cli/commit/1055b49))





## [5.1.1](https://github.com/ionic-team/ionic-cli/compare/ionic@5.1.0...ionic@5.1.1) (2019-06-26)

**Note:** Version bump only for package ionic





# [5.1.0](https://github.com/ionic-team/ionic-cli/compare/ionic@5.0.3...ionic@5.1.0) (2019-06-21)


### Bug Fixes

* **start:** fix glitch with writing package.json without spaces ([389c398](https://github.com/ionic-team/ionic-cli/commit/389c398))
* subsequent validation for various prompts ([1b92f8a](https://github.com/ionic-team/ionic-cli/commit/1b92f8a))


### Features

* **info:** show available updates for utilities ([a9f4b54](https://github.com/ionic-team/ionic-cli/commit/a9f4b54))
* replace update-notifier ([a232c07](https://github.com/ionic-team/ionic-cli/commit/a232c07))
* **deploy:** command to interactively add deploy plugin ([#4039](https://github.com/ionic-team/ionic-cli/issues/4039)) ([c75e66f](https://github.com/ionic-team/ionic-cli/commit/c75e66f))





## [5.0.3](https://github.com/ionic-team/ionic-cli/compare/ionic@5.0.2...ionic@5.0.3) (2019-06-18)


### Bug Fixes

* **capacitor:** use correct web-dir path for react and capacitor ([#4029](https://github.com/ionic-team/ionic-cli/issues/4029)) ([cdf2579](https://github.com/ionic-team/ionic-cli/commit/cdf2579))
* **cordova:** always generate resources when adding platforms ([3220b2f](https://github.com/ionic-team/ionic-cli/commit/3220b2f))
* **cordova:** don't append --save to platform/plugin management commands ([#4028](https://github.com/ionic-team/ionic-cli/issues/4028)) ([0356d00](https://github.com/ionic-team/ionic-cli/commit/0356d00))
* **cordova:** warn about missing cordova-res when adding platforms ([77fa904](https://github.com/ionic-team/ionic-cli/commit/77fa904))





## [5.0.2](https://github.com/ionic-team/ionic-cli/compare/ionic@5.0.1...ionic@5.0.2) (2019-06-10)


### Bug Fixes

* **capacitor:** use dist for --web-dir for vue/capacitor ([#4012](https://github.com/ionic-team/ionic-cli/issues/4012)) ([0979715](https://github.com/ionic-team/ionic-cli/commit/0979715))
* **cordova:** fix --project flag for cordova commands ([fb9ff0f](https://github.com/ionic-team/ionic-cli/commit/fb9ff0f))
* **cordova:** invoke native-run in integration root ([526eda3](https://github.com/ionic-team/ionic-cli/commit/526eda3))





## [5.0.1](https://github.com/ionic-team/ionic-cli/compare/ionic@5.0.0...ionic@5.0.1) (2019-06-05)


### Bug Fixes

* **cordova:** add port forwarding for --consolelogs ([d2e0c81](https://github.com/ionic-team/ionic-cli/commit/d2e0c81))
* **cordova:** pass --device to native-run if specified ([5db46d5](https://github.com/ionic-team/ionic-cli/commit/5db46d5))





# [5.0.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.12.0...ionic@5.0.0) (2019-05-29)

At a glance, this is what was changed or added in this major release of the Ionic CLI:

* Support for **Ionic React** (beta) :rocket: (`ionic start --type=react`)
* [`native-run`](https://github.com/ionic-team/native-run) is used to deploy app binaries to devices for `ionic cordova run`
* [`cordova-res`](https://github.com/ionic-team/cordova-res) is used to generate Cordova resources locally for `ionic cordova resources`
* `localhost` is now the default host for `ionic serve`, `ionic cordova run -l`, and `ionic capacitor run -l`
    * Port forwarding via `native-run` is used for connected Android devices
    * For iOS hardware devices, you may need to serve your app externally with `--address=0.0.0.0`
* `--devapp` is now a required flag if you want to use DevApp with `ionic serve`
* `--consolelogs` for Angular projects is now available for `ionic cordova run -l`
* Command completion is available for ZSH users (`ionic completion --help`) (see [#2482](https://github.com/ionic-team/ionic-cli/issues/2482) for bash)
* CLI source code targets modern JS, resulting in noticable speed improvements

#### :lollipop: Upgrading from CLI 4

Make sure you have NodeJS v8.9.4+ installed. We recommend [the latest LTS version](https://nodejs.org/).

Install the [`cordova-res`](https://github.com/ionic-team/cordova-res) and [`native-run`](https://github.com/ionic-team/native-run) utilities.

```
npm i -g cordova-res native-run
```

For Angular 8 projects, make sure you have the latest `@ionic/angular-toolkit` installed.

```
npm i @ionic/angular-toolkit@latest
```

For Angular 7 projects, make sure you have the [latest 1.x](https://www.npmjs.com/package/@ionic/angular-toolkit?activeTab=versions) `@ionic/angular-toolkit` installed.

```
npm i @ionic/angular-toolkit@1
```


### Bug Fixes

* **capacitor:** send --npm-client param to capacitor init ([#3963](https://github.com/ionic-team/ionic-cli/issues/3963)) ([44b0918](https://github.com/ionic-team/ionic-cli/commit/44b0918))
* **cordova:** prefer plugged-in devices, be explicit with Cordova ([ef8296b](https://github.com/ionic-team/ionic-cli/commit/ef8296b))
* **doctor:** relax the viewport regex ([d0bc021](https://github.com/ionic-team/ionic-cli/commit/d0bc021))
* **open:** fix unbound listener ([e63b74a](https://github.com/ionic-team/ionic-cli/commit/e63b74a))
* **prepare:** check config and platforms dir for platform state ([d9e1ced](https://github.com/ionic-team/ionic-cli/commit/d9e1ced))
* **react:** support react git repo ([#3982](https://github.com/ionic-team/ionic-cli/issues/3982)) ([c06857f](https://github.com/ionic-team/ionic-cli/commit/c06857f))


### chore

* **serve:** `--devapp` required for DevApp ([5ad11ef](https://github.com/ionic-team/ionic-cli/commit/5ad11ef))
* **serve:** remove `--local` option ([806eaaa](https://github.com/ionic-team/ionic-cli/commit/806eaaa))
* **serve:** switch default host to `localhost` ([d2a32de](https://github.com/ionic-team/ionic-cli/commit/d2a32de))
* require Node 8 ([5670e68](https://github.com/ionic-team/ionic-cli/commit/5670e68))


### Features

* **cordova:** handle lack of port forwarding in ios ([d68faf1](https://github.com/ionic-team/ionic-cli/commit/d68faf1))
* add -v as shortcut for --version ([d917e8e](https://github.com/ionic-team/ionic-cli/commit/d917e8e))
* **start:** add conference and my-first-app starter templates for angular ([#3978](https://github.com/ionic-team/ionic-cli/issues/3978)) ([ea26181](https://github.com/ionic-team/ionic-cli/commit/ea26181))
* Add React project type ([#3936](https://github.com/ionic-team/ionic-cli/issues/3936)) ([ef852fa](https://github.com/ionic-team/ionic-cli/commit/ef852fa))
* **angular:** Ionic 4 commands no longer beta ([16be793](https://github.com/ionic-team/ionic-cli/commit/16be793))
* **cordova:** check for `native-run` before running ([89ffd21](https://github.com/ionic-team/ionic-cli/commit/89ffd21))
* **cordova:** instructions on how to fix faulty Android SDKs ([ce87944](https://github.com/ionic-team/ionic-cli/commit/ce87944))
* **cordova:** use `cordova-res` by default ([83e48cf](https://github.com/ionic-team/ionic-cli/commit/83e48cf))
* **cordova:** use `native-run` by default ([eadcba0](https://github.com/ionic-team/ionic-cli/commit/eadcba0))
* **help:** color refactor ([5938429](https://github.com/ionic-team/ionic-cli/commit/5938429))
* **info:** native-run and cordova-res versions ([d6af864](https://github.com/ionic-team/ionic-cli/commit/d6af864))
* **login:** authenticate using stdin ([d88529f](https://github.com/ionic-team/ionic-cli/commit/d88529f))
* **serve:** support `--consolelogs` for cordova serve in angular projects ([#3900](https://github.com/ionic-team/ionic-cli/issues/3900)) ([17f1438](https://github.com/ionic-team/ionic-cli/commit/17f1438))
* Command-Line Completions ([9f66512](https://github.com/ionic-team/ionic-cli/commit/9f66512))


### BREAKING CHANGES

* **cordova:** `ionic cordova resources` no longer generates resources
using Ionic servers by default. Instead, `cordova-res` is used to
generate resources locally. PSD and AI file formats are no longer
supported in this new flow. The old behavior is available by specifying
`--no-cordova-res`.
* **cordova:** `ionic cordova run/emulate` no longer use Cordova to
deploy apps by default. `cordova run`, which builds and deploys the app,
is no longer used. Instead, `cordova build` is used to build the app and
then it is deployed to devices using `native-run`. The old behavior is
available by specifying `--no-native-run`. When using Cordova to run,
unless you manually forward ports, you will need to also specify
`--address=0.0.0.0` (or any host accessible externally).
* **serve:** For DevApp usage, the `--devapp` flag is now required
for all project types, instead of being automatic. This change was made
in conjunction with changing the default host from `0.0.0.0` to
`localhost`. By explicitly specifying `--devapp`, however, `0.0.0.0` is
used if `--address` is not specified.
* **serve:** `ionic serve` and other commands using the dev server
will no longer be hosted on the BIND ALL address (0.0.0.0) by default.
`localhost` is the new default. The old behavior is available by passing
`--address=0.0.0.0`.
* **serve:** The `ionic serve --local` option is now irrelevant. The default address is
changing to `localhost`.
* A minimum of Node.js 8.9.4 is required.
* **help:** option/command/namespace groups are now `MetadataGroup`





<a name="4.12.0"></a>
# [4.12.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.11.0...ionic@4.12.0) (2019-03-12)


### Features

* **enterprise:** add shortcut for registering ([a1890b4](https://github.com/ionic-team/ionic-cli/commit/a1890b4))
* add `i` as alias for `integrations` ([14a7ddb](https://github.com/ionic-team/ionic-cli/commit/14a7ddb))
* **integrations:** add `--web-dir` option for capacitor integration ([#3895](https://github.com/ionic-team/ionic-cli/issues/3895)) ([8a1c4b2](https://github.com/ionic-team/ionic-cli/commit/8a1c4b2))
* **integrations:** ionic enterprise integration ([#3905](https://github.com/ionic-team/ionic-cli/issues/3905)) ([b071fcb](https://github.com/ionic-team/ionic-cli/commit/b071fcb))




<a name="4.11.0"></a>
# [4.11.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.10.4...ionic@4.11.0) (2019-03-06)


### Features

* **cordova:** add experimental `--cordova-res` flag ([16cdef8](https://github.com/ionic-team/ionic-cli/commit/16cdef8))
* **cordova:** add experimental `--native-run` flag ([a80d465](https://github.com/ionic-team/ionic-cli/commit/a80d465))




<a name="4.10.4"></a>
## [4.10.4](https://github.com/ionic-team/ionic-cli/compare/ionic@4.10.3...ionic@4.10.4) (2019-02-27)




**Note:** Version bump only for package ionic

<a name="4.10.3"></a>
## [4.10.3](https://github.com/ionic-team/ionic-cli/compare/ionic@4.10.2...ionic@4.10.3) (2019-02-15)




**Note:** Version bump only for package ionic

<a name="4.10.2"></a>
## [4.10.2](https://github.com/ionic-team/ionic-cli/compare/ionic@4.10.1...ionic@4.10.2) (2019-02-04)


### Bug Fixes

* **angular:** pass `--project` and `--configuration` for custom scripts ([2cf724f](https://github.com/ionic-team/ionic-cli/commit/2cf724f))




<a name="4.10.1"></a>
## [4.10.1](https://github.com/ionic-team/ionic-cli/compare/ionic@4.10.0...ionic@4.10.1) (2019-01-30)


### Bug Fixes

* **cordova:** only forward correct options ([817879b](https://github.com/ionic-team/ionic-cli/commit/817879b))




<a name="4.10.0"></a>
# [4.10.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.9.0...ionic@4.10.0) (2019-01-29)


### Bug Fixes

* **ionic-angular:** link to proper v3 docs ([a89c097](https://github.com/ionic-team/ionic-cli/commit/a89c097))


### Features

* **serve:** add DevApp support for Ionic 4 projects ([#3830](https://github.com/ionic-team/ionic-cli/issues/3830)) ([6edf373](https://github.com/ionic-team/ionic-cli/commit/6edf373))




<a name="4.9.0"></a>
# [4.9.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.8.0...ionic@4.9.0) (2019-01-23)


### Features

* **custom:** run ionic:build/ionic:serve scripts ([9898fa8](https://github.com/ionic-team/ionic-cli/commit/9898fa8))
* **resources:** --cordova-res option for local resource generation ([3c27e05](https://github.com/ionic-team/ionic-cli/commit/3c27e05))
* **start:** make Ionic 4 the default for new projects ([#3820](https://github.com/ionic-team/ionic-cli/issues/3820)) ([0195f96](https://github.com/ionic-team/ionic-cli/commit/0195f96))




<a name="4.8.0"></a>
# [4.8.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.7.1...ionic@4.8.0) (2019-01-14)


### Features

* **appflow:** command to create deploy builds ([#3815](https://github.com/ionic-team/ionic-cli/issues/3815)) ([d346e03](https://github.com/ionic-team/ionic-cli/commit/d346e03))




<a name="4.7.1"></a>
## [4.7.1](https://github.com/ionic-team/ionic-cli/compare/ionic@4.7.0...ionic@4.7.1) (2019-01-08)




**Note:** Version bump only for package ionic

<a name="4.7.0"></a>
# [4.7.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.6.0...ionic@4.7.0) (2019-01-07)


### Bug Fixes

* **doctor:** handle multilines for viewport-fit-not-set ([#3809](https://github.com/ionic-team/ionic-cli/issues/3809)) ([6aa7ae6](https://github.com/ionic-team/ionic-cli/commit/6aa7ae6))
* **executor:** Exclude options for command argument parsing ([#3798](https://github.com/ionic-team/ionic-cli/issues/3798)) ([514015f](https://github.com/ionic-team/ionic-cli/commit/514015f))
* **serve:** handle error in opn with debug statement ([89b6d33](https://github.com/ionic-team/ionic-cli/commit/89b6d33))


### Features

* **appflow:** command to create package builds ([#3808](https://github.com/ionic-team/ionic-cli/issues/3808)) ([149f06e](https://github.com/ionic-team/ionic-cli/commit/149f06e))
* **cordova:** auto-forward port when using --native-run ([0da50ac](https://github.com/ionic-team/ionic-cli/commit/0da50ac))




<a name="4.6.0"></a>
# [4.6.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.5.0...ionic@4.6.0) (2018-12-19)


### Bug Fixes

* **cordova:** warn for prepare w/o platforms ([385bdf2](https://github.com/ionic-team/ionic-cli/commit/385bdf2))


### Features

* **serve:** collapse numbered chunk output and summarize ([5ac6834](https://github.com/ionic-team/ionic-cli/commit/5ac6834))
* **start:** update for Ionic Framework 4.0 RC ([7e943cc](https://github.com/ionic-team/ionic-cli/commit/7e943cc))




<a name="4.5.0"></a>
# [4.5.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.4.0...ionic@4.5.0) (2018-11-27)


### Bug Fixes

* **cordova:** do not error for ctrl+c during livereload ([facc96b](https://github.com/ionic-team/ionic-cli/commit/facc96b))
* **serve:** ignore link-local addresses ([#3761](https://github.com/ionic-team/ionic-cli/issues/3761)) ([1b7fd90](https://github.com/ionic-team/ionic-cli/commit/1b7fd90))
* **telemetry:** disable automatically for CI ([217ca12](https://github.com/ionic-team/ionic-cli/commit/217ca12))


### Features

* Ionic Appflow rebranding ([16360af](https://github.com/ionic-team/ionic-cli/commit/16360af))
* **cordova:** add `--native-run` option to Cordova run ([#3757](https://github.com/ionic-team/ionic-cli/issues/3757)) ([9ef53ad](https://github.com/ionic-team/ionic-cli/commit/9ef53ad))




<a name="4.4.0"></a>
# [4.4.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.3.1...ionic@4.4.0) (2018-11-20)


### Bug Fixes

* **multi-app:** properly handle bare projects ([3f84a6f](https://github.com/ionic-team/ionic-cli/commit/3f84a6f)), closes [/github.com/ionic-team/ionic-docs/issues/83#issuecomment-439655706](https://github.com//github.com/ionic-team/ionic-docs/issues/83/issues/issuecomment-439655706)
* **project:** write determined project type to config ([307d81f](https://github.com/ionic-team/ionic-cli/commit/307d81f))


### Features

* **build:** show build progress ([3090615](https://github.com/ionic-team/ionic-cli/commit/3090615))
* **help:** show value hint for options ([aa13ba8](https://github.com/ionic-team/ionic-cli/commit/aa13ba8))
* **init:** add `ionic init` command ([4a12b17](https://github.com/ionic-team/ionic-cli/commit/4a12b17))
* **login:** SSO authentication flow ([#3741](https://github.com/ionic-team/ionic-cli/issues/3741)) ([71b319a](https://github.com/ionic-team/ionic-cli/commit/71b319a))
* **serve:** forward `--ssl` to Angular CLI ([815b49a](https://github.com/ionic-team/ionic-cli/commit/815b49a))




<a name="4.3.1"></a>
## [4.3.1](https://github.com/ionic-team/ionic-cli/compare/ionic@4.3.0...ionic@4.3.1) (2018-11-04)


### Bug Fixes

* **bin:** stringify unresolved promise event ([788a5ec](https://github.com/ionic-team/ionic-cli/commit/788a5ec))
* **bootstrap:** supply env for CLI <4.3.0 ([78dbda8](https://github.com/ionic-team/ionic-cli/commit/78dbda8))
* **multi-app:** hide project warnings during start ([b1ecd77](https://github.com/ionic-team/ionic-cli/commit/b1ecd77))
* **start:** fix stdio freezing issue on Windows ([#3725](https://github.com/ionic-team/ionic-cli/issues/3725)) ([a570770](https://github.com/ionic-team/ionic-cli/commit/a570770))




<a name="4.3.0"></a>
# [4.3.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.2.1...ionic@4.3.0) (2018-10-31)


### Bug Fixes

* **capacitor:** switch off livereload for --no-build ([9960047](https://github.com/ionic-team/ionic-cli/commit/9960047))
* **help:** filter out unnecessary global options ([7809c99](https://github.com/ionic-team/ionic-cli/commit/7809c99))
* **ssh:** adjust validator to work for OpenSSH 7.8 ([dcc598a](https://github.com/ionic-team/ionic-cli/commit/dcc598a))
* **terminal:** adjust some feature detection on windows ([8a2ed99](https://github.com/ionic-team/ionic-cli/commit/8a2ed99))


### Features

* **capacitor:** add --livereload-url option for custom dev server ([b7738f5](https://github.com/ionic-team/ionic-cli/commit/b7738f5))
* **cordova:** add --livereload-url option for custom dev server ([ad57e36](https://github.com/ionic-team/ionic-cli/commit/ad57e36))
* **integrations:** --root option for choosing an alternative location ([7e8f11e](https://github.com/ionic-team/ionic-cli/commit/7e8f11e))
* **multi-app:** determine active project via cwd path match ([f83dc5b](https://github.com/ionic-team/ionic-cli/commit/f83dc5b))
* **resources:** generate resources without needing platform installation ([4f20554](https://github.com/ionic-team/ionic-cli/commit/4f20554))
* **start:** better multi-app support ([3c70e87](https://github.com/ionic-team/ionic-cli/commit/3c70e87))




<a name="4.2.1"></a>
## [4.2.1](https://github.com/ionic-team/ionic-cli/compare/ionic@4.2.0...ionic@4.2.1) (2018-10-05)


### Bug Fixes

* **doctor:** fix viewport-fit-not-set for ionic1 ([826b9ae](https://github.com/ionic-team/ionic-cli/commit/826b9ae))
* **info:** show versions for [@ionic](https://github.com/ionic)/angular-toolkit ([9d1824a](https://github.com/ionic-team/ionic-cli/commit/9d1824a))




<a name="4.2.0"></a>
# [4.2.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.1.2...ionic@4.2.0) (2018-10-03)


### Bug Fixes

* **cordova:** ng should ignore separated args for Cordova build ([16a0111](https://github.com/ionic-team/ionic-cli/commit/16a0111))
* **lab:** use correct query params for project type ([4801680](https://github.com/ionic-team/ionic-cli/commit/4801680))
* **serve:** fix incorrect message about app-scripts not being installed ([abd665b](https://github.com/ionic-team/ionic-cli/commit/abd665b))
* **serve:** unnecessary message about utility CLI exiting during Ctrl+C ([8e78bf3](https://github.com/ionic-team/ionic-cli/commit/8e78bf3))


### Features

* new `ionic repair` command ([7588233](https://github.com/ionic-team/ionic-cli/commit/7588233))




<a name="4.1.2"></a>
## [4.1.2](https://github.com/ionic-team/ionic-cli/compare/ionic@4.1.1...ionic@4.1.2) (2018-09-05)


### Bug Fixes

* **capacitor:** use integration root for Capacitor CLI ([81a45d5](https://github.com/ionic-team/ionic-cli/commit/81a45d5))




<a name="4.1.1"></a>
## [4.1.1](https://github.com/ionic-team/ionic-cli/compare/ionic@4.1.0...ionic@4.1.1) (2018-08-20)


### Bug Fixes

* **cordova:** respect --nosave for platform/plugin add ([eb4934b](https://github.com/ionic-team/ionic-cli/commit/eb4934b))
* **deploy:** exclude any existing pro-manifest.json files ([#3527](https://github.com/ionic-team/ionic-cli/issues/3527)) ([d03057d](https://github.com/ionic-team/ionic-cli/commit/d03057d))
* **shell:** allow output() to fail with original error ([e6a5bff](https://github.com/ionic-team/ionic-cli/commit/e6a5bff))
* **shell:** check if process is still alive before sending signal ([0ff1e48](https://github.com/ionic-team/ionic-cli/commit/0ff1e48))




<a name="4.1.0"></a>
# [4.1.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.0.6...ionic@4.1.0) (2018-08-15)


### Bug Fixes

* **capacitor:** pass in project/package id during start ([1357c5c](https://github.com/ionic-team/ionic-cli/commit/1357c5c))
* **cordova:** properly error for multiple IPs with non-interactive mode ([0346adc](https://github.com/ionic-team/ionic-cli/commit/0346adc))
* **cordova:** remove unwanted allow-navigation entries ([77984e1](https://github.com/ionic-team/ionic-cli/commit/77984e1))
* **info:** disable update check for cordova cli ([8310ff6](https://github.com/ionic-team/ionic-cli/commit/8310ff6))
* **info:** remove version.json warning for v1 ([78c3582](https://github.com/ionic-team/ionic-cli/commit/78c3582))
* **link:** support new repo association types ([1c1e1f1](https://github.com/ionic-team/ionic-cli/commit/1c1e1f1))


### Features

* **capacitor:** add run command ([62a2918](https://github.com/ionic-team/ionic-cli/commit/62a2918))
* **capacitor:** document platform argument, prompt when required ([2a312ab](https://github.com/ionic-team/ionic-cli/commit/2a312ab))
* **capacitor:** install platform if missing ([9e29235](https://github.com/ionic-team/ionic-cli/commit/9e29235))
* **capacitor:** prompt for supported platforms when adding ([54c7d55](https://github.com/ionic-team/ionic-cli/commit/54c7d55))
* **capacitor:** unlock capacitor commands as beta ([2480a01](https://github.com/ionic-team/ionic-cli/commit/2480a01))
* **info:** print whitelisted cordova plugins ([c266b7b](https://github.com/ionic-team/ionic-cli/commit/c266b7b))




<a name="4.0.6"></a>
## [4.0.6](https://github.com/ionic-team/ionic-cli/compare/ionic@4.0.5...ionic@4.0.6) (2018-08-09)


### Bug Fixes

* **serve:** fix unclosed connection issue again ([#3500](https://github.com/ionic-team/ionic-cli/issues/3500)) ([1f0ef3b](https://github.com/ionic-team/ionic-cli/commit/1f0ef3b))




<a name="4.0.5"></a>
## [4.0.5](https://github.com/ionic-team/ionic-cli/compare/ionic@4.0.4...ionic@4.0.5) (2018-08-07)




**Note:** Version bump only for package ionic

<a name="4.0.4"></a>
## [4.0.4](https://github.com/ionic-team/ionic-cli/compare/ionic@4.0.3...ionic@4.0.4) (2018-08-06)


### Bug Fixes

* **serve:** properly cleanup child processes ([#3481](https://github.com/ionic-team/ionic-cli/issues/3481)) ([38217bf](https://github.com/ionic-team/ionic-cli/commit/38217bf))




<a name="4.0.3"></a>
## [4.0.3](https://github.com/ionic-team/ionic-cli/compare/ionic@4.0.2...ionic@4.0.3) (2018-08-02)


### Bug Fixes

* **build:** prompt to install "build cli" for all projects ([2862762](https://github.com/ionic-team/ionic-cli/commit/2862762))
* **serve:** await connectivity on specified host, not localhost ([#3444](https://github.com/ionic-team/ionic-cli/issues/3444)) ([bf10674](https://github.com/ionic-team/ionic-cli/commit/bf10674))
* **serve:** check all network interfaces for an available port ([30fd6ef](https://github.com/ionic-team/ionic-cli/commit/30fd6ef))
* **serve:** fix --livereload for device/emulator ([f31e79d](https://github.com/ionic-team/ionic-cli/commit/f31e79d))
* **serve:** use correct livereload port option for v1 ([bf3e775](https://github.com/ionic-team/ionic-cli/commit/bf3e775))




<a name="4.0.2"></a>
## [4.0.2](https://github.com/ionic-team/ionic-cli/compare/ionic@4.0.1...ionic@4.0.2) (2018-07-30)


### Bug Fixes

* **cordova:** default to `cordova prepare` without platforms ([d40d961](https://github.com/ionic-team/ionic-cli/commit/d40d961))
* **resources:** fix hanging issue ([#3429](https://github.com/ionic-team/ionic-cli/issues/3429)) ([6b7c732](https://github.com/ionic-team/ionic-cli/commit/6b7c732))
* **build:** properly pass --target to remove fonts for cordova ([530d87a](https://github.com/ionic-team/ionic-cli/commit/530d87a))
* **generate:** run in current directory ([54c632b](https://github.com/ionic-team/ionic-cli/commit/54c632b))
* **info:** filter out hidden files/folders ([2e56dd7](https://github.com/ionic-team/ionic-cli/commit/2e56dd7))
* **info:** show 'not available' when cordova is missing ([db60879](https://github.com/ionic-team/ionic-cli/commit/db60879))




<a name="4.0.1"></a>
## [4.0.1](https://github.com/ionic-team/ionic-cli/compare/ionic@4.0.0...ionic@4.0.1) (2018-07-26)


### Bug Fixes

* **generate:** remove pages/ prefix recommendation ([#3392](https://github.com/ionic-team/ionic-cli/issues/3392)) ([23d0db6](https://github.com/ionic-team/ionic-cli/commit/23d0db6))
* **help:** properly show option decorations ([b2509de](https://github.com/ionic-team/ionic-cli/commit/b2509de))




<a name="4.0.0"></a>
# [4.0.0](https://github.com/ionic-team/ionic-cli/compare/ionic@4.0.0-rc.13...ionic@4.0.0) (2018-07-25)




**Note:** Version bump only for package ionic

This release offers support for :sparkles: **Ionic 4** :sparkles: (beta).

:memo: Use the new [CLI Documentation](https://beta.ionicframework.com/docs/cli) on the beta framework documentation website for CLI 4.

#### :lollipop: Upgrading from CLI 3

Aside from a few edge cases listed below, upgrading to CLI 4 should be seamless.

**Ionic 2/3**: The CLI will continue working with apps using `@ionic/app-scripts` for tooling (please [update to the latest version](https://github.com/ionic-team/ionic-app-scripts) to avoid any issues). The CLI will continue to support projects that have yet to migrate to Ionic 4 w/ Angular CLI for tooling. For those who wish to migrate v3 apps to v4, see the [Migration Guide](https://beta.ionicframework.com/docs/building/migration).

**Ionic 1**: For Ionic 1 projects, a new toolkit has been introduced to slim down the main CLI package. All functionality is still supported, but the `@ionic/v1-toolkit` package needs to be installed.

#### :boom: Breaking Changes

* Support for legacy Ionic Cloud ended on January 31st, 2018. The `ionic upload` and `ionic package` commands have been removed from the CLI. Support for [Ionic Appflow](https://ionicframework.com/appflow/) will be a major focus for the CLI going forward. :ok_hand:
* The `app_id` property in `ionic.config.json` has been renamed to `pro_id` and is now optional (see [#3038](https://github.com/ionic-team/ionic-cli/issues/3038)). The CLI automatically detects this and changes it, but this notice is here if your build scripts rely on the setting.
* `ionic build` will no longer run `cordova prepare`. Instead, run `ionic cordova prepare <platform>`, which performs an Ionic build beforehand.
* `ionic cordova prepare` will no longer run an Ionic build without a platform, e.g. `ionic cordova prepare ios` (see [#3653](https://github.com/ionic-team/ionic-cli/issues/3653))
* Ionic Lab has been moved into the [`@ionic/lab`](https://github.com/ionic-team/ionic-cli/tree/develop/packages/@ionic/lab) package, which will need to be installed for Lab to work.
* The `conference` starter template has been removed from `ionic start`. To clone existing apps (as opposed to starting new apps from starter templates), please use the app's repository URL. For example, to create the conference app, use `ionic start "Conference App" https://github.com/ionic-team/ionic-conference-app`.
* The `--display-name` option for `ionic start` has been removed. The `name` argument is now used as the display name and slugified for directory name, package name, etc. To provide a custom slug, use `--project-id` (see [#3038](https://github.com/ionic-team/ionic-cli/issues/3038)).
* The `ionic:watch:before` npm script hook has been renamed to `ionic:serve:before`, but behaves the same.
* `ionic doctor check` will now _only_ print issues and exit with exit code 1 if issues are found. Use `ionic doctor treat` to attempt automatic fixes.
* `ionic doctor ignore` has been removed in favor of `ionic config set -g doctor.issues.<issue>.ignored true`).
* Ionic 1 build/serve functionality has been moved into the [`@ionic/v1-toolkit`](https://github.com/ionic-team/ionic-cli/tree/develop/packages/@ionic/v1-toolkit) package, which will need to be installed in your Ionic 1 project(s). The file watcher, [chokidar](https://github.com/paulmillr/chokidar), has been updated to 2.0.0, which will require those using `watchPatterns` to [always use POSIX-style slashes](https://github.com/paulmillr/chokidar/blob/master/CHANGELOG.md#chokidar-200-dec-29-2017) (not an issue if you've never used a backslash in globs for Windows).
* The gulp integration has been removed from the CLI and put into the [`@ionic/v1-toolkit`](https://github.com/ionic-team/ionic-cli/tree/develop/packages/@ionic/v1-toolkit) package, which is only for Ionic v1 apps.

#### :rocket: Enhancements

* `ionic s` is now an alias for `ionic serve`.
* No need for `@ionic/cli-plugin-proxy`. Proxy support is now built-in. Use existing environment variables or use `ionic config set -g proxy <url>`.
* New `ionic config unset` command for deleting config values.
* New `ionic doctor treat` command that attempts automatic fixes of detected issues.
* If `ionic:build` or `ionic:serve` npm scripts are defined in your `package.json`, the Ionic CLI will use them for the Ionic build/serve instead of the default for your project type.
* Automatic login via `IONIC_TOKEN` environment variable [#2410](https://github.com/ionic-team/ionic-cli/issues/2410)
* `--no-color` flag for turning off CLI colors
* `--no-build` option for `ionic cordova run` and `ionic cordova emulate` [#2930](https://github.com/ionic-team/ionic-cli/pull/2930)
* Better monorepo support. See the discussion in [#2232](https://github.com/ionic-team/ionic-cli/issues/2232).
* Multi-app support for new Angular projects [#3281](https://github.com/ionic-team/ionic-cli/issues/3281)
* Added experimental `ionic ssl generate` command for generating `localhost` SSL certificates for use with `ionic serve`. :memo: HTTPS support in `ionic serve` isn't quite finished yet (see [#3305](https://github.com/ionic-team/ionic-cli/issues/3305)).

#### :bug: Bug Fixes

* Interactivity is now disabled when not in a TTY. See [#3047](https://github.com/ionic-team/ionic-cli/issues/3047).
* Respect `--nosave` flag for `ionic cordova platform` and `ionic cordova plugin` [#2946](https://github.com/ionic-team/ionic-cli/issues/2946)
* Chain `--verbose` flag to Cordova for `ionic cordova` commands [#2919](https://github.com/ionic-team/ionic-cli/issues/2919)
* Fixed newlines in piped output from underlying CLIs.

#### :house: Internal

* A huge amount of code refactoring has been accomplished to prepare the CLI for a scalable, flexible future. Changes in behavior and help output based upon environment and config are now trivially accomplished.
* The [CLI Framework](https://github.com/ionic-team/ionic-cli/tree/develop/packages/%40ionic/cli-framework), a (currently) internal framework for building general-purpose command-line programs, has had many features added to support the utility CLIs such as `ionic-lab` and `ionic-v1`.
* Ionic Lab has been rebuilt using [StencilJS](https://stenciljs.com) and now works for any Ionic Framework version.

## Older Changes

* [3.x `CHANGELOG.md`](https://github.com/ionic-team/ionic-cli/blob/3.x/CHANGELOG.md)
* [1.x-2.x `CHANGELOG.md`](https://github.com/ionic-team/ionic-cli/blob/2.x/CHANGELOG.md)
