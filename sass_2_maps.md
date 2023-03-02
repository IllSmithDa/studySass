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

  