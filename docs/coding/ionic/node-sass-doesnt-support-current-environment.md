# Node Sass does not yet support your current environment: Windows 64-bit with Unsupported runtime (115)

## Issue Faced:

![node sass does not support current environment](/img/node-sass-does-not-support-current-environment.png)


## Solution:

- this is because your PC node.js version too latest and your project node version too old.

- either u need to downgrade the node.js or upgrade the node-sass

- for the upgrade node-sass command:

`npm uninstall node-sass && npm install node-sass`