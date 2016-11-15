_Managing tutorial samples_
### Sample 1 - KendoUI-skeleton-esnext
| [Original source code](https://github.com/aurelia/skeleton-navigation/tree/master/skeleton-esnext)| [Matching KendoUI sample](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/tree/master/skeleton-esnext) |

#### Step 1 - add KendoUI bridge

Assuming that the original source code was successfuly built and executed by

```
npm install && jspm install && gulp watch
```

the KendoUI bridge is added by running

```
jspm install aurelia-kendoui-bridge
```

#### Step 2 - add source code using KendoUI bridge

This sample uses **[JSPM](https://aurelia-ui-toolkits.gitbooks.io/kendo-ui-sdk-installation/content/installation/installing%20kendo/advanced/core/jspm.html)** module loader and adds two "widgets" **`Autocomplete`** and **`Button`** from  **[KendoUI Core](https://aurelia-ui-toolkits.gitbooks.io/kendo-ui-sdk-installation/content/installation/installing%20kendo/kendo_core.html)** package  to the standard Skeleton-esnext application, by adding the [**`kendoui`** folder](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/tree/master/skeleton-esnext/src/kendoui) to the original application's **`src`** folder.

This added folder's content is:

1. [**`autocomplete`**](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/tree/master/skeleton-esnext/src/kendoui/autocomplete)
 - [`autocomplete.html`](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/src/kendoui/autocomplete/autocomplete.html)
  - [`autocomplete.js`](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/src/kendoui/autocomplete/autocomplete.js)
<br><br>

2. [**`button`**](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/tree/master/skeleton-esnext/src/kendoui/button)

  - [`button.html`](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/src/kendoui/button/button.html)

  - [`button.js`](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/src/kendoui/button/button.js)

  - [`button.css`](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/src/kendoui/button/button.css)


#### Step 3 - add KendoUI widgets

It is custom to keep the thrid party packages in the vendors folder, so we need to create this folder and add the needed KendoUI code.

#### Step 4 - modifying various existing files

##### Step 4.1 - [index.html](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/index.html)

Add these **[three scripts](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/index.html#L18-L21)**

```
<!-- Kendo-SDK files -->
<script src="kendo-sdk/js/jquery.min.js"></script>
<script src="kendo-sdk/js/jszip.min.js"></script>
<script src="kendo-sdk/js/kendo.all.min.js"></script>
```

___Note: the line `<script src="kendo-sdk/js/kendo.all.min.js"></script>` is a temporary placeholder - it will be replaced with `kendo.custom.min.js` created to include only KendoUI widgets actually used in the application___.

##### Step 4.2 - [package.json](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/package.json)

Add the reference to **[`aurelia-kendoui-bridge`](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/package.json#L73)**

##### Step 4.3 -  [Changes to prevent JSPM from loading JQuery](https://aurelia-ui-toolkits.gitbooks.io/kendoui-bridge-docs/content/app_developer_notes/prevent_jspm_from_loading_jquery.html)

- Run `jspm install bootstrap -o "{ dependencies: {} }"`
- Add **[this line](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/config.js#L27)** to **[config.js](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/blob/master/skeleton-esnext/config.js)**

***