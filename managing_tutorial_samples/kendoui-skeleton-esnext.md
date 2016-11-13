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

This sample uses **[JSPM](https://aurelia-ui-toolkits.gitbooks.io/kendo-ui-sdk-installation/content/installation/installing%20kendo/advanced/core/jspm.html)** module loader and adds two "widgets" **`Autocomplete`** and **`Button`** from  **[KendoUI Core](https://aurelia-ui-toolkits.gitbooks.io/kendo-ui-sdk-installation/content/installation/installing%20kendo/kendo_core.html)** package  to the standard Skeleton-esnext application, by adding the **`kendoui`** folder to the original application's **`src`** folder as shown on Image 1 below

<p align=center>
  <img src="https://cloud.githubusercontent.com/assets/2712405/20242496/ba3747c4-a8fd-11e6-8bc9-593ac142dfa8.png"></img>
 <br><br>
Image 2
</p>

where:

**`autocomplete.html`**
```
<template>
  <section>
    <br>
    <h3>Basic KendoUI Autocomplete sample</h3>

    <a href="https://github.com/aurelia-ui-toolkits/aurelia-kendoui-plugin/tree/master/sample/src/samples/autocomplete">See KendoUI Bridge autocomplete folder for more details</a>
    <br>
    <br>

    <p><strong>People:</strong></p>
    <ak-autocomplete k-data-source.bind="items">
        <input style="width: 100%;">
    </ak-autocomplete>
    <br>
    <br>
    <br>
    <p class="demo-hint" style="word-break: break-all">Type a name, available values in the list are: ${ items } </p>
  </section>
</template>
```

<br>

**`autocomplete.js`**
```
export class BasicUse {
  items = [
    'Charles',
    'Jedd',
    'Nikolaj',
    'Jeroen',
    'David',
    'Rob',
    'Matt',
    'Patrick',
    'Jason',
    'Martin',
    'Fredrick',
    'Alex'
  ]
}
```

<br>

**`button.html`**
```
<template>
    <require from="./button.css"></require>
    <section>
        <br>
        <h3>Basic KendoUI Button API sample</h3>

        <a href="https://github.com/aurelia-ui-toolkits/aurelia-kendoui-plugin/tree/master/sample/src/samples/button">See KendoUI Bridge button folder for more details</a>
        <br>
        <br>

        &nbsp;&nbsp;<button ak-button="k-icon: ungroup; k-widget.bind: button" k-on-click.delegate="test()">Kendo UI Button</button>
        <br>
        <br>
        <button ak-button click.delegate="button.enable(false)">Disable</button>
        &nbsp;&nbsp;
        <button ak-button click.delegate="button.enable(true)">Enable</button>

    </section>
</template>
```

<br>

**`button.js`**
```
export class ButtonApi {
    test() {
      alert('You clicked me');
    }
}
```

<br>

**`button.css`**
```
#button .demo-section {
    text-align: center;
}
#button .box .k-textbox {
    margin: 0;
    width: 80px;
}
```

#### Step 3 - add KendoUI widgets

It is custom to keep the thrid party packages in the vendors folder, so we need to create this folder and add the needed KendoUI code.


