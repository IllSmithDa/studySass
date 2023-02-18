# Nesting in Sass

  1. Sass nesting is much more intuitive than the standard way which would be for the follow where p tag is inside the main div 

  e.g 
  .main {
    width: 80%;
    margin: 0 auto;
  }
  .main p {
    color: #222222;
  }

  2. Instead of adding a new set of definitions and brackets simply place the p tag inside of the main directly. Its makes the files more compact and wordy

  e.g 
  .main {
    width: 80%;
  
    p {
      color: #222222;
    }
  }

  3. You can also nest other classes as well assuming you have nested elements with a class in them 

  e.g.

  .main {
    width: 90%;
    .title-class {
      font-weight: 600;
    }
  }

  4. If you have __class name nested in a element you can use operator '#{&}' to denote it in sass 

  e.g 
  .main {
    width: 80%;
    
    /* uses '#{&}' in place of 'main' for the nested class name */
    #{&}__paragraph {
      font-weight: 700;

      /* '&:' used to indicate a different state for css which is hover */
      &:hover {
        color: pink
      }
    }
  }