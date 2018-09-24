# Annotation UI

## Instructions to add this library to your own angular app
https://www.npmjs.com/package/hmcts-annotation-ui-lib

Check demo app:
https://github.com/hmcts/rpa-annotation-ui-demo


Import AnnotationUiLibModule from annotation-ui-lib in your app.module.ts and declare it in your NgModule imports.

For example:
```
import { AnnotationUiLibModule, ViewerComponent} from 'hmcts-annotation-ui-lib';

@NgModule({
  imports: [
    ...
    AnnotationUiLibModule
  ]
})
```

Reference the followings scripts in your angular.json.
```
"scripts": [
    "node_modules/hmcts-annotation-ui-lib/assets/shared/pdf.js",
    "node_modules/hmcts-annotation-ui-lib/assets/shared/pdf_viewer.js",
    "node_modules/hmcts-annotation-ui-lib/assets/shared/pdf-annotate.js",
    ...
]
```

And styles
```
"styles": [
  "node_modules/hmcts-annotation-ui-lib/_theme.scss",
  ...
],
```

Entry point is the ViewerComponent component. For example:
```
const appRoutes: Routes = [
  { path: '',  component: ViewerComponent }
]; 
```

Make sure to pass a query parameter for the PDF location when you navigate to the component. For example:
Copy your PDF into the root assets folder and reference it like http://localhost:4200?url=/assets/example.pdf


## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/?url=/assets/example.pdf`. The app will automatically reload if you change any of the source files.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
