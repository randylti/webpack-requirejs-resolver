# requirejs-resolver

Allows using `import` to find modules based on requirejs config path mapping.

This is specifically useful for Magento 2, which extensively uses requirejs.

## Config parsing

The config file is executed to find all calls to `require.config()`.

## Usage

    const RequireJsResolverPlugin = require('@sdinteractive/requirejs-resolver');

    module.exports = {
      resolve: {
        plugins: [
          new RequireJsResolverPlugin({
            configPath: path.resolve(__dirname, 'requirejs-config.js'),
          }),
        ],
      },
    };
