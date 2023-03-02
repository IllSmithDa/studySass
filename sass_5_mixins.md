# Mixins in Sass

  1. Mixins allow to define a set of css properties that can be reused throughout your app. 
     Use the keyword '@mixin' followed by a name. Mixins should be used for a set properties
     that is being commonly reused in your application

    e.g
    @mixin flexCenter {
      display: flex;
      justify-content: center;
      align-items: center;
    }

  2. To add mixin into existing css, just use operator 'include' followed by the name of the defined mixin 

    .main {
      @include flexCenter;
      width: 88%;
      margin: 0 auto;
    }

  3. You can add parameters to mixins which can be used to further define certain properties 

    e.g
    @mixin xMargins($flexVal) {
      margin-left: $flexVal;
      margin-right: $flexVal;
    }

    .main {
      @include flexCenter(auto)
    }

      a. As you can see, mixins are function like but are specifically used to style properties while
      functions are used to test and retireve values which will be used to assign css property values

# Mixin Use Cases 

  1. One classic use case for mixins is adding theme such as dark theme vs light
     theme in application. Note that in this example, we set a default value for
     the parameter as true. We also have a if statement which will check if
     light theme is set to true. 
  
  2. Note that the lighten and darken are built in functions in SASS that will return 
     a darker or lighter version of that particular color and the intensity of the change 
     is given as a percentage in the second parameter of the function
  
      a. src: https://falkus.co/2017/05/using-lighten-and-darken-in-sass/

    e.g
    @mixin them($light-theme: true) {
      @if (light-theme) {
        background: lighten($primary-color, 100%);
        color: darken($text-color, 100%);
      }
    }

    .light {
      include theme($light-theme: true);
    }

      a. Here we are using the theme function in the light class and we are passing true in the parameters. 
      $light-theme is optional but can be good for clarity. 


  3. If compilier finds a empty block of code, it will not do anything. Make sure you have your 
     cases covered when working with functions

    e.g
    @mixin them($light-theme: true) {
      @if (light-theme) {
        background: lighten($primary-color, 100%);
        color: darken($text-color, 100%);
      }
    }

      a, Only light theme is covered 

    e.g
    @mixin theme($light-theme: true) {
      @if ($light-theme) {
        background: lighten($accent-color, 10%);
        color: darken($text-color, 10%);
      } @else {
        background: darken($accent-color, 10%);
        color: lighten($text-color, 10%);
      }
    }

      a. we now have both light and dark themes covered

# Media Queries and Mixins

  1. Here we have a mixin combined with a media query. '@media()' paremeter
     'max-width' defined using variable '$mobile' and includes a keyword
     '@content' which is allows for custom css properties to be passed into 
     the media query and in this case is 'flex-direction.' 

    e.g
    $mobile: 800;
    @mixin mobile {
      @media (max-width: $mobile) {
        @content
      }
    }

    .main {
      @include mobile {
        display: flex
        flex-direction: column
      }
    }