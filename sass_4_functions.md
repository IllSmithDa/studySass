# Functios in Sass

  1. You can also create functions in sass using '@function'

  2. Here is a function that takes weight-name and searches the map for the corresponding value 
  and returns it

    e.g 
    @function weight($weight-name) {
      @return map-get($font-weights, $weight-name);
    }

  3. You can call the function like you would a regular javascript function 

    e.g 
    p {
      font-weight: weight(bold);
    }
  
      a. weight() function is called and is used a key to return the corresponding value