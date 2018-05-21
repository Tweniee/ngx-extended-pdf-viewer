# Ng6PdfViewer

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.0.0.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Update to the newest version of the core PDF library:

* git clone https://github.com/legalthings/pdf.js.git
* cd pdf.js
* npm install
* gulp generic
* cd ..

And update the files from source and patch them

* cd pdf.js-viewer
* npm install
* ./build.sh ../pdf.js/build/generic/

* copy `viewer.css` to `inlineImageFiles/assets/viewer.css`
* replace every "html " by "htmlignore " (the trailing space is important!)
* replace every "body " by "bodyignore " (the trailing space is important!)
* replace every "url('images" by "url('assets/images"
* run `node.js index.js` from the `inlineImageFiles` folder
* copy the file `viewer-with-images.css` to the folder `projects/ngx-extended-pdf-viewer/src/lib`

Run `npm run package` to build the library (from the root directory of the project). The build artifacts will be stored in the `dist/ngx-extended-pdf-viewer` directory.

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

Note to the author: to deploy the library on npm, change to the folder `dist/ngx-extended-pdf-viewer` and run `npm publish` from there.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
