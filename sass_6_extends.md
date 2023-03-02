# Extending css to other css

  1. Sass gives you the option to extend css classes to other css. This is
     useful if you want to extend other css classes while having the option
     to have additional css properties. Paragraph 2 will now extend all the 
     properties of paragraph 1

    e.g 
    .main {
      #{&}_paragraph1 {
        font-weight: weight(bold);
        &hover {
          color: pink
        }
      }

      #{&}_paragraph2 {
        @extend .main_paragraph1;
      }
    }