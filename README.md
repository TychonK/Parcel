# Parcel starter kit
Easy to use template for front-end projects. Insists on parcel bundler.

SASS preproccessor is set by default for stylization. No need for any additional extension to be installed for CSS complilation.

*Customly made by TychonK*

## Before starting work

### Dependencies
An LTS-version of [Node.js](https://nodejs.org/en/) with all additional tools except for **Chocolatey** (this is not nessesary) has to be installed on your PC. 

### Hidden files and folders
Turn on showing hidden files and folders in your public opinion explorer, otherwise you won't
you can select and find project settings files whose names begin with points of view.

### Finally
Install all dependencies once per project

```shell
npm ci
```

## Development server
The development server is started by executing:

```shell
npm run start
``` 
command in the terminal. 
The bundler will compile a live version of the website and host it on `http://localhost:<port>` with an available port (default port: `1234`).

## Production build
To build an optimized production version of your website, execute:

```shell
npm run build
```
The files in the `dist` folder will be deleted and replaced with those created during the build. 
In order to do this, navigate to the file `package.json` and edit the line `homepage` by changing `user_name` and `repository_name` on your own.

```json
"homepage": "https://<user_name>.github.io/<repository_name>",
"scripts": {
  "build": "parcel build src/*.html --public-url ./"
},
```

Just in case, it is reasonable to navigate through `Settings` > `Pages` and make sure that
production versions of the files are hosted on `/root` of branch `gh-pages`.

After certain period of time, live page will be available by the link noted in the edited property `homepage`, for example
[https://TychonK.github.io/parcel-starter-kit](https://TychonK.github.io/parcel-starter-kit).

## Deployment
The kit will automatically build and deploy the production version of the project to github-pages branch, every time when the main branch is updated. For example, after a direct commit or an accepted pull-request. 

## Files and folders work

- All styles partials have to be located at `src/sass` 
  and be imported at `src/sass/main.scss`
- Images should be added to `src/images`, optimize them in advance.