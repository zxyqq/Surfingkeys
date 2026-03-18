# 2026/3/18
在当前窗口执行后，将所有窗口中和它相同的域名的都移动到一个新的窗口
当前在surfingkeys中提供了如下2个映射可组合达到效果，
能否做到一个新的函数一步达到效果呢
        mapkey('W', '#3Move current tab to another window',  function() {
            front.openOmnibar(({type: "Windows"}));
        });

        mapkey(';gt', '#3Gather filtered tabs into current window', function() {
            front.openOmnibar({type: "Tabs", extra: {
                action: "gather"
            }});
        });


## install fnm/npm
cargo install fnm
fnm install --lts
fnm use lts-latest

## npm use taobao mirror
npm config set registry https://registry.npmmirror.com/

## npm install skip puppeteer
PUPPETEER_SKIP_DOWNLOAD=true npm install --verbose
npm install --verbose

遇到问题单独install了如下4个包
npm install --save-dev @babel/runtime --verbose
npm install --save-dev events @types/node
npm install --save-dev events @types/node
npm install terser-webpack-plugin --save-dev
对应会修改 package.json, 已经提交到 dev 分支


## build/crx
npm run build:prod

npm install -g crx  
crx pack dist/production/chrome/ -o surfingkeys.crx
