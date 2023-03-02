# Math Operations in Sass

  1. Sass allows you to perform Math calcaultions on your css properties that involve numerical values

    e.g
    .main {
      width: 80% - 40%;
    }

  2. Normal css allow you to do operations as well using the keyword 'calc()' and even using pixels mixed with percentage. You cannot mix types in SASS. 

    e.g 
    .main {
      width: cal(80% - 400px);
    }

