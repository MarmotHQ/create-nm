# create-nm

[![NPM version][npm-image]][npm-url]
[![Build status][travis-image]][travis-url]
[![Coverage status][codecov-image]][codecov-url]
[![Dependency status][daviddm-image]][daviddm-url]
[![CircleCI](https://circleci.com/gh/MarmotHQ/create-nm.svg?style=svg)](https://circleci.com/gh/MarmotHQ/create-nm)

`npm init nm` to create a **n**pm **m**odule.

> Never manually do the linting, versioning, tagging, editing changelog and pushing commit, unleash the power of hooks.

## Create a npm module

- use `npm`

```bash
# choose one of the following methods
$ npm init nm [name]
$ npx create-nm [name]
$ npm i -g create-nm && create-nm [name]
```

- use `yarn`

```bash
$ yarn create nm [name]
```

## Workflow of publishing a npm module

Commit and publish, everything will be done automatically.

```bash
$ git commit
$ npm publish
```

```
                       +-------------------+
version :  1.1.0       |                   |
    tag : v1.1.0       |   $ git commit    |
                       |                   |
                       +--+----------------+
                          |
                          +-> lint-staged

                       +-------------------+
                       |                   |
                       |   $ git commit    |
                       |                   |
                       +--+----------------+
                          |
                          +-> lint-staged

                                 +
                                 |
                                 |
                                 |
                                 v

                       +-------------------+
                       |                   |
version :  1.1.1       |  $ npm publish    |
    tag : v1.1.1       |                   |
                       +--+----------------+
                          |
                          |   update npm version
                          |   update CHANGELOG.md
                          |   commit version with changelog
                          +-> add git tag
                              git push commit
                              npm publish
```

## Optional workflow

Use `git cz` instead of `git commit`, this will generate better changelog.
You need to install `commitizen` and create `~/.czrc`.

```bash
$ npm install commitizen -g
$ echo '{ "path": "cz-conventional-changelog" }' > ~/.czrc
```

Workflow:

```bash
$ git cz
$ npm publish
```

## Related

- [np](https://github.com/sindresorhus/np) A better `npm publish`.
- [commitizen](https://github.com/commitizen/cz-cli) Simple commit conventions for internet citizens.
- [conventional-changelog](https://www.npmjs.com/package/conventional-changelog-cli) Generate a changelog from git metadata.
- [lint-staged](https://github.com/okonet/lint-staged) Lint files staged by git.
- [husky](https://github.com/typicode/husky) Prevents bad commit or push (git hooks, pre-commit/precommit, pre-push/prepush, post-merge/postmerge and all that stuff...)].

## Contributors

[![](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/images/0)](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/links/0)[![](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/images/1)](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/links/1)[![](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/images/2)](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/links/2)[![](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/images/3)](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/links/3)[![](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/images/4)](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/links/4)[![](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/images/5)](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/links/5)[![](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/images/6)](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/links/6)[![](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/images/7)](https://sourcerer.io/fame/zhangyuheng/MarmotHQ/create-nm/links/7)

## License

[MIT](http://opensource.org/licenses/MIT)

[npm-image]: https://img.shields.io/npm/v/create-nm.svg?style=flat-square&logo=npm
[npm-url]: https://npmjs.org/package/create-nm
[travis-image]: https://img.shields.io/travis/MarmotHQ/create-nm/master.svg?style=flat-square&logo=travis
[travis-url]: https://travis-ci.org/MarmotHQ/create-nm
[codecov-image]: https://img.shields.io/codecov/c/github/MarmotHQ/create-nm/master.svg?style=flat-square&logo=javascript
[codecov-url]: https://codecov.io/gh/MarmotHQ/create-nm
[daviddm-image]: https://img.shields.io/david/MarmotHQ/create-nm.svg?style=flat-square
[daviddm-url]: https://david-dm.org/MarmotHQ/create-nm
