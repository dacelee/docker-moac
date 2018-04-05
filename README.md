# docker-moac
MOAC docker image based on ubuntu 1604 x64

# relates
https://github.com/MOACChain

# usage
- supporting staff
  - [redis-server]
    - needed by mining pool backend proxies and api
  - [nginx]
    - needed by mining pool frontend web page
- moac wallet/console/vnode
  - /root/moac [--testnet] [--rpc [--rpcaddr 0.0.0.0]] [--mine] [console]
- moac vnode mining proxies and/or api
  - [customize]
    - /root/config.json
  - [run]
    - redis-server &
    - /root/open-moac-mining /root/config.json

- frontend webpages for vnode mining / api endpoints / payments
  - [customize]
    - /root/build/open-moac-pool/www/config/environment.js
  - [build]
    - nvm install --lts=carbon ; npm install -g bower;  cd /root/build/open-moac-pool/www; git pull; rm -fr dist; npm install ; bower install --allow-root; ./build.sh
  - [web]
    - nginx

# you can read online https://github.com/lospringliu/docker-moac
