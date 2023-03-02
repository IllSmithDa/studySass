# Documentation

  1. https://sass-lang.com/documentation/

# There are two different type of syntax for Sass

  1. Scss syntax 

    a. uses the file extension .scss

    b. It is superset of css which means all valid css is also valid scss. 

    c. Its simlarity to css makes it more popular and quicker to learn and pick up 
  
  2. Sass syntax

    a. Also known as the indented syntax 

    b. same as scss but uses indentation instead of curly braces and semi-colons

    c. similar style to python coding perhaps

# Sass Settings and Installation 

  1. You can search for Sass compiler inculding 'Live Sass Compiler' which will help comiple sass into css which is what is readable for the web application 

  2. Click on the cogwheel on the bottom left of visual studio code and find settings. 

  3. On Settings page, click on extensions, search and click on Sass 

  3. Find the first setting.json which will allow you to adding custom setting in the json file
     and will be used to set the sprecific output file in a specific directory
  
  4. set the following setting in the settings.json file to set the save output file into the dist/css folder 

    e.g
    "liveSassCompile.settings.formats": [
       {
           "format": "expanded",
           "extensionName": ".css",
           "savePath": "~/../dist/css",
       },
     ]

  5. After you create your scss main file in the project directory, you can
     click on the watch sass button the on bottom blue bar next to the line
     and column number section of VS Cdoe.


# Basics 

1. Plain css works just fine for scss. When working with sass, you should never manipulate the css file itself because the compiler will always overwrite the css file

  e.g
  body {
    background: blue;
  }

# Variables in Sass

  1. Sass allow you to use variables. So does Css. While CSS variables are mostly compatible with 
  browsers, sass is superior because its varaibles don't compile to variables at all but to actual 
  values making them more easily readible and compatible with browsers than css
  variables 
  
    e.g
    :root {
      --primary-color: #272727;
    }

    body {
      background: var(--primary-color);
    }

      a. classic css variable syntax

  2. Check out the simplicity of the sass variable syntax

    $primary-color: #272727;

    body {
      background: $primary-color;
    }

# Maps in Sass

  1. You can use a key value pairs in sass if you want to set several possible key values for a 
  particular css property such as the font-weight. It is useful when you want to narrow a few 
  key values for settings that have many possible numeric values such as font-weight or colors

    $font-weights: (
      "regular": 400,
      "medium": 500,
      "bold": 700
    );

  2. Note you need to add ; at the end or it will produce an error

  3. You can then use the map-get(name, key) to set a value from a map to css property. Here we 
  set h1 font-weight to the map and retrieve the value for bold property from the font-weights map

    e.g
    h1 {
      font-weight: map-get($font-weights, bold);
    }

  