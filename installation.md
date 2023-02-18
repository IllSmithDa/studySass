# Sass Settings and Installation 

  1. You can search for Sass compiler inculde 'Live Sass Compiler' which will help comiple sass into css which is what is readable for the web application 

  2. Click on the cogwheel on the bottom left of visual studio code and find settings. 

  3. On Settings page, click on extensions, search and click on Sass 

  3. Find the first setting.json which will allow you to adding custom setting in the json file
     
     and will be used to set the sprecific output file in a specific directory
  
  4. set the following setting in the settings.json file to set the save output file into 

     the dist/css folder 

    e.g

    "liveSassCompile.settings.formats": [
       {
           "format": "expanded",
           "extensionName": ".css",
           "savePath": "~/../dist/css",
       },
     ]

   5. After you create your scss main file in the project directory, you can click on the watch 

      sass button the on bottom blue bar next to the line and column number section of VS Cdoe.
