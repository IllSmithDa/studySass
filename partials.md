# Separating Files 

  1. With Sass, we can create partial css files that include snippets of css that we can 
  include into other files

  2. Its a greate way to compartmentalize and increase ease of maintainability of css 

  3. With that being said, partials are simply scss files with a underscore line in front of the name.

  4. Partials let's comilper know not to generate a css file from the file because its just a partial which will be imported into a full sass file that will be compiled into css 

  5. Example partial file name and file content with some resets in it
  e.g 
  _headers.scss
  
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  6. To include this partial, find the file you want to import into and use keyword '@import' followed by the file path. Note in the example below, you don't include the underscore or 
  the .scss file type into the import

  e.g

  @import './headers';

  7. One use case for partials is that you can store all your variables in a partial and import them to whatever files you need without channging the syntax of the scss files. Just make sure 
  to import the partial files and you can use the varaibles as normal