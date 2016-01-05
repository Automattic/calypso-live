# Calypso Live Branches

A proxy server which checkouts a branch of your web application and runs it on demand.

## Usage

A demo for [Calypso](https://github.com/Automattic/wp-calypso) is available in the Makefile, type `make run` to launch it.

## TODO:

- [x] Code refactoring and comments.
- [x] Display a page while instance is installing.
- [x] Remove application specific code in `worker.js` (ie `make build` and `require('build/bundle-development.js');`).
- [x] Monitor workers: restart failed workers (or mark them as failing for this commit), shutdown unused workers.
- [ ] Find alternatives to `require` to launch the server with the patch on `net.Server.listen` (needed so we can proxy it); have a look at [`node-sandboxed-module`](https://github.com/felixge/node-sandboxed-module) or [`pm2`](https://github.com/Unitech/pm2). 
- [ ] Create a Dockerfile.
