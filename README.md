# Picasso Qlik Sense Extension Template
## New: Now with brushing/selections
Here you can find JS code to be used as a starting point for a Qlik Sense *Picasso extension*, an extension which makes use of the open-sourced rendering engine picassojs.com by Qlik.

Compared to my first version released under gihub repository "qs-ext-picasso-emptystart", this one installs as a <b>Qlik Sense Extension Template</b>. This means, you don't see a new extension after installing, but need use this template for a new extension. It also contains necessary code snippets to allow brushing and selections. See below. 

The new extension will only show "Hello PicassoJS" as a text first. That is, because it is meant to be replaced with some more exciting examples from picassojs.com or your own chart definition. 

1) Download this extension package as a ZIP and extract it to your Qlik Sense Desktop extension folder or, if on a Sense Server, import it with the QMC
2) Go to the address http://localhost:4848/dev-hub (or /dev-hub on your Sense server) and click on "New Extension", choose "picasso-template" from the list

![alt text](https://github.com/ChristofSchwarz/qs-ext-template-picasso/raw/master/screenshot-extension-editor.png "Screenshot")

* Note that there are also some example chart extensions copied and opened in the Extenions editor, like 'sample-stack-area.js' and 'sample-range-area.js' which you can use as cheetsheets to write your own working javascript

* here is my video Part 1 where I explain the steps so far https://youtu.be/KRADE-GXCf4 (just be clear, that the "Duplicate Extension" step is replaced by "New from template" since this is a template type of extension).

3) To start your own chart, just remove the "Hello PicassoJS" line between the down triangles ▼▼▼ and up triangles ▲▲▲ where it reads "components: [...]
4) Best place to try out the settings in a what you see it what you get manner is the "Examples" section on https://picassojs.com This will take you to  https://beta.observablehq.com (the playground page behind) 
5) When done, copy/paste your Json definitions (the settings-object and possible custom functions) into your mypicasso1.js file from this package where the inline-comments tell you. Adjust the hypercube size, number of measures and dimensions accordingly.
* here is my video Part 2, where I explain the process https://youtu.be/ZYjmO-oAFyM
* <b>NEW!</b> To enable brushing (making selections) some more lines of code are required, shared in this repository. Video to explain it is here https://youtu.be/hedEyOwrqvE

Screenshots:
![alt text](https://github.com/ChristofSchwarz/qs-ext-template-picasso/raw/master/Screenshot.png "Screenshot")

### Note on NPM INSTALL (Updated for April-2018 release)
This code will run out of the box as I bundled a version of both, picasso.js and picasso-plugin-q into this extension (subfolder node_modules). I do no longer load the interal versions of picasso.js preinstalled with Qlik Sense and you don't have to uncomment /comment rows in the extension. I recommend to download the latest versions of Picasso.js and Picasso-Q-Plugin using NPM INSTALL (part of NodeJS installation). 

* Go to the relative root folder on Qlik Sense Desktop in a Command Prompt. In the above example the extension is here: "C:\Users\yourid\Documents\Qlik\Sense\Extensions\mypicasso1"
* type "npm install picasso.js"
* type "npm install picasso-plugin-q"
* you will get updated versions below subfolder "node_modules" and more version informations.

### Resources:
* To learn about PicassoJS see https://picassojs.com and https://github.com/qlik-oss/picasso.js
* A sample app is also provided in here (*.qvf) which has sample data for the sample-stack-area chart and sample-range-area chart like in the screenshot above.
* Blog by Thomas Gorr with advanced examples, custom components, tool tips etc found here https://thomasgorr.wordpress.com/2018/09/03/experimenting-with-picassojs/

