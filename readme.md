# next-neutron

Working next + neutron + electron combo with (as of today) latest versions:
```
"electron": "^7.1.9",
"next": "^9.2.0",
"react": "^16.12.0",
"react-dom": "^16.12.0"
```

```
Node v10.16.3
Npm v6.9.0
```

This is a new Electron app created with [Neutron](https://www.npmjs.com/package/neutron).

Neutron github repo seems to be private, so couldn't fork it. Link leads to npmjs.

## Monkey-patch for node_modules/neutron with patch-package

Since I couldn't fork neutron on github, this repo includes a monkey-patch for neutron to support Next 9.X.X.

## Builds from root

The regular version of neutron expects nextjs-code to be located in /renderer. In this repo neutron grabs out dir from root. This means you can:
- Build the project regularly with `next build` & `next export` and publish to Now
- Build the project for Mac / Windows using Electron with `neutron build`

## How to get going

`npm install`

`npm run dev` (next: to develop as usual using the browser)

`npm run build` (to build .next)

`npm run electron-dev` (to develop in-electron window)

`npm run electron-build` (to build  .exe/.app into /apps)

## Published to Zeit Now

[next-neutron.now.sh](https://next-neutron.now.sh)
