# Managing tutorial samples

This article documents the process of creating and managing the content described in the section **[4. Application Developer tutorials](https://aurelia-ui-toolkits.gitbooks.io/kendoui-bridge-docs/content/developers_tutorials.html)** from the **[Aurelia KendoUI Bridge Documentation](https://aurelia-ui-toolkits.gitbooks.io/kendoui-bridge-docs/content/)**

In order to ensure the best possible syncronization between the Aurelia's **[skeleton navigation samples](https://github.com/aurelia/skeleton-navigation)** used as the basis for KendoUI bridge's own (parallel) set of **[KendoUI tutorials code](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code)**, the information in **[4. Application Developer tutorials](https://aurelia-ui-toolkits.gitbooks.io/kendoui-bridge-docs/content/developers_tutorials.html)** ___describes the process of modifying Aurelia samples___ to be able to use KendoUI bridge.

This article explains the creation and management of the **[kendoui-tutorials-code](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code)** repository which contains the finished code for samples as tutorials in the section **[4. Application Developer tutorials](https://aurelia-ui-toolkits.gitbooks.io/kendoui-bridge-docs/content/developers_tutorials.html)**. The process is very similar for all entries in **[kendoui-tutorials-code](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code)** repository:

##### Step 1 
Copy the code of the original navigation skeleton sample from **[skeleton-navigation](https://github.com/aurelia/skeleton-navigation)** sample to **[kendoui-tutorials-code](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code)**

##### Step 2
Transform the original code in just the created **[kendoui-tutorials-code](https://github.com/aurelia-ui-toolkits/kendoui-tutorials-code)** repository to add all changes needed to make this sample use KendoUI bridge.

The specifics of each transformation are described on the following pages:

[1. KendoUI-skeleton-esnext](./managing_tutorial_samples/kendoui-skeleton-esnext.html)

[2 KendoUI-skeleton-esnext-aspnetcore](./managing_tutorial_samples/kendoui-skeleton-esnext-aspnetcore.html)

[3. KendoUI-skeleton-esnext-webpack](./managing_tutorial_samples/kendoui-skeleton-esnext-webpack.html)

[4. KendoUI-skeleton-typescript](./managing_tutorial_samples/kendoui-skeleton-typescript.html)

[5. KendoUI-skeleton-typescript-aspnetcore](./managing_tutorial_samples/kendoui-skeleton-typescript-aspnetcore.html)

[6. KendoUI-skeleton-typescript-webpack](./managing_tutorial_samples/kendoui-skeleton-typescript-webpack.html)

Each of the above pages shows what needs to be changed in order to add a few additional tabs which render Aurelia KendoUI components: 

- **`Autocomplete`** and **`Button`** tabs to illustrate the use of **[KendoUI Core](https://aurelia-ui-toolkits.gitbooks.io/kendo-ui-sdk-installation/content/installation/installing%20kendo/kendo_core.html)**

<p align=center>
  <img src="https://cloud.githubusercontent.com/assets/2712405/20317317/8368b0ce-ab33-11e6-83c7-26e140d6ed3e.png"></img>
 <br>
Image 1
</p>

 <br>

   <p align=center>
  <img src="https://cloud.githubusercontent.com/assets/2712405/20317378/ca66a49a-ab33-11e6-9a19-7aa442a712a3.png"></img>
 <br><br>
Image 2
</p>


<br>
- **`Chart`** and **`Grid`** tabs to illustrate the use of **[KendoUI Pro](https://aurelia-ui-toolkits.gitbooks.io/kendo-ui-sdk-installation/content/installation/installing%20kendo/kendo_pro.html)**

  <p align=center>
  <img src="https://cloud.githubusercontent.com/assets/2712405/20317448/18ab9c50-ab34-11e6-9465-10919f9a5192.png"></img>
 <br>
Image 3
</p>

  <br>

  <p align=center>
<img src="https://cloud.githubusercontent.com/assets/2712405/20317495/47e7a0a4-ab34-11e6-8c82-1807b729e1fa.png"></img>
 <br>
Image 4
</p>

***
***



