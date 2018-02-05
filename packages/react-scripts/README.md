## albert-react-scripts

My version tracks the offical react-scripts stable version (currently v1.1.0) with a couple of differences, here is the code [diff](https://github.com/facebookincubator/create-react-app/compare/react-scripts@1.1.0...albertstill:albert-react-scripts@1.0.1) on GitHub.

- Added [CSS Modules](https://github.com/css-modules/css-modules), [`postcss-import`](https://github.com/postcss/postcss-import) and [`postcss-cssnext`](https://github.com/MoOx/postcss-cssnext). Note I removed `autoprefixer` because it's included in `postcss-cssnext`.
- Allow consumers to set their own Babel config, they must have a `.babelrc` or `babel` field in their package.json. I required this to use the Relay Modern plugin on a side project. Because [`babel-preset-react-app`](https://github.com/facebookincubator/create-react-app/tree/master/packages/babel-preset-react-app) is really good I recommend doing `yarn add babel-preset-react-app` and adding the preset `echo '{ "presets": ["react-app"] }' > .babelrc`, that way your config can be a superset of the offical [config](https://github.com/facebook/create-react-app/blob/react-scripts%401.1.0/packages/react-scripts/config/webpack.config.prod.js#L178).

`create-react-app --scripts-version albert-react-scripts my-app && cd my-app && yarn add babel-preset-react-app && echo '{ "presets": ["react-app"] }' > .babelrc && yarn run start`
