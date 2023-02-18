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

# Basics 

1. Plain css works just fine for scss. When working with sass, you should never manipulate the css file itself because the compiler will always overwrite the css file

e.g in main.scss
body {
  background: blue;
}

# Variables in Sass

  1. Sass allow you to use variables. So does Css. While CSS variables are mostly compatible with 
  browsers, sass is superior because its varaibles don't compile to variables at all but to actual 
  values making them more easily readible and compatible with browsers than css variables 

  e.g classic css variable syntax

  :root {
    --primary-color: #272727;
  }

  body {
    background: var(--primary-color);
  }

  2. Check out the simplicity of the sass variable syntax

    $primary-color: #272727;

    body {
      background: $primary-color;
    }
