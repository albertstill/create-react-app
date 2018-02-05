## albert-react-scripts

The same as the official react-scripts@master with a couple of [differences](https://github.com/facebookincubator/create-react-app/compare/master...albertstill:master):

- Added [CSS Modules](https://github.com/css-modules/css-modules), [`postcss-import`](https://github.com/postcss/postcss-import) and [`postcss-cssnext`](https://github.com/MoOx/postcss-cssnext). Note I removed `autoprefixer` because it's included in `postcss-cssnext`.
- Removed the hardcoded Babel presets/plugins. Consumers should have their own `.babelrc` or `babel` field in their package.json. I required this to use the Relay Modern plugin in a side project. Because [`babel-preset-react-app`](https://github.com/facebookincubator/create-react-app/tree/master/packages/babel-preset-react-app) is really good I recommend doing `yarn add babel-preset-react-app` and adding the preset `echo '{ "presets": ["react-app"] }' > .babelrc`, that way your new config can be a superset of the offical config.
