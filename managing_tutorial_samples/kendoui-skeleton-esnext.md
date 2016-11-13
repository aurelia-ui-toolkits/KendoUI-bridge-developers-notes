_Managing tutorial samples_
### Sample 1 - KendoUI-skeleton-esnext
| [Original source code](https://github.com/aurelia/skeleton-navigation/tree/master/skeleton-esnext)| [Matching KendoUI sample](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code/tree/master/skeleton-esnext) |

#### Step 1 - add KendoUI bridge

```
λ npm install aurelia-kendoui-bridge
aurelia-skeleton-navigation@1.1.1 C:\work\aurelia-ui-toolkits\kendoui\kendoui-tutorials-code\skeleton-esnext
`-- aurelia-kendoui-bridge@1.0.1

npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@^1.0.0 (node_modules\chokidar\node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.0.15: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})
```


This sample uses **[JSPM](https://aurelia-ui-toolkits.gitbooks.io/kendo-ui-sdk-installation/content/installation/installing%20kendo/advanced/core/jspm.html)** module loader and **[KendoUI Core](https://aurelia-ui-toolkits.gitbooks.io/kendo-ui-sdk-installation/content/installation/installing%20kendo/kendo_core.html)** package and adds the **`Autocomplete`** and **`Button`** tabs to the standard Skeleton-esnext application, by adding the **`kendoui`** folder to the original application's **`src`** folder as shown on Image 1 below

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



