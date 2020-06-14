# WEBPACK-COURSE
mkdir src dist config
git init
npm init -y -> crates package.json

echo "node_modules" .gitignore
npm install -g webpack webpack-cli
echo > src/index.js 
echo > dist/index.html
webpack --node=development
webpack --node=production
echo > config/webpack.dev.js

del /f src\index.js
del /f dist\main.js

echo > config/webpack.dev.js

Edit the dist/index.html
const path = require('path')
module.exports= {
    entry: {
        main: "./src/main.js"
    },
    mode: "development",
    output: {
        filename: "[name]-bundle.js",
        path: path.resolve(__dirname,"../dist")
    }
}

webpack --config=config/webpack.dev.js
