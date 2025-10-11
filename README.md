#Notes from freeCodeCamp to add as comments on CSS file

##Step 8 
browsers calculate the size of container elements in a way that extends image borders beyond its container
The box-sizing property is used to set this behavior. By default, the content-box model is used. With this model, when an element has a specific width, that width is calculated based only on the element's content. Padding and border values get added to the total width, so the element grows to accommodate these values.

##Step 9
Change the box-sizing property to border-box. Notice how your blue image borders now fit within your red gallery border.

##Step 13
Make the text uppercase using the text-transform property with uppercase as the value.

##Step 20
Rather than setting each aspect ratio individually to fix distortion, you can use the object-fit property to determine how images should behave.
Give your .gallery img selector the object-fit property and set it to cover. This will tell the image to fill the img container while maintaining aspect ratio, resulting in cropping to fit.