## Honorable Mentions:

## Step 4
Screen readers announce HTML elements based on the document flow. We will eventually want the balance sheet to have a heading of "Balance Sheet" and a subheading of "AcmeWidgetCorp". However, this order does not make sense if announced by a screen reader.

Give your existing span the class attribute set to flex, and add two span elements within it. Give the first the text AcmeWidgetCorp. Give the second the text Balance Sheet. You will use CSS to reverse the order of the text on the page, but the HTML order will make more sense for a screen reader.

## Step 5
Below your h1 element, create a div element. Give it an id attribute set to years. You want this particular element to be hidden from screen readers, so give it the aria-hidden attribute set to true.

## Step 11
Within each of your new th elements, nest a span element with the class set to sr-only year. Give them the following text (in order): 2019, 2020, and 2021.

Give your third th element the class attribute set to current.

Leave the td element empty. This element exists only to ensure your table has a four-column layout and associate the headers with the correct columns.

## Step 30
Before you get too far into your styling, you should make use of the sr-only class. You can use CSS to make elements with this class completely hidden from the visual page, but still be announced by screen readers.

The CSS you are about to write is a common set of properties used to ensure elements are completely hidden visually.

The span[class~="sr-only"] selector will select any span element whose class includes sr-only. Create that selector, and give it a border property set to 0.

## Step 31
The CSS clip property is used to define the visible portions of an element. Set the span[class~="sr-only"] selector to have a clip property of rect(1px, 1px, 1px, 1px).

The clip-path property determines the shape the clip property should take. Set the clip-path property to the value of inset(50%), forming the clip-path into a rectangle within the element.

## Step 33
To prevent the text content from overflowing, give your span[class~="sr-only"] selector an overflow property set to hidden and a white-space property set to nowrap.


## Step 34
Finally, you need to take these hidden elements out of the document flow. Give the span[class~="sr-only"] selector a position property set to absolute, a padding property set to 0, and a margin property set to -1px. This will ensure that not only are they no longer visible, but they are not even within the page view.

## Step 37
The :first-of-type pseudo-selector is used to target the first element that matches the selector. Create an h1 .flex span:first-of-type selector to target the first span element in your .flex container. Remember that your span elements are reversed, visually, so this will appear to be the second element on the page.

Give your new selector a font-size property of 0.7em to make it look like a sub-heading.

## Step 38
The :last-of-type pseudo-selector does the exact opposite - it targets the last element that matches the selector. Create an h1 .flex span:last-of-type selector to target the last span in your flex container, and give it a font-size property set to 1.2em to make it look like a header.

## Step 39
You wrapped your table in a section element - now you can style that to give your table a border. Create a section selector, and give it a max-width property set to 40rem for responsive design. Set the margin property to 0 auto to center it, and set the border property to 2px solid #d0d0d5.

## Step 42
The calc() function is a CSS function that allows you to calculate a value based on other values. For example, you can use it to calculate the width of the viewport minus the margin of an element:

Example Code
.example {
  margin: 10px;
  width: calc(100% - 20px);
}
Give #years a margin of 0 -2px, and a padding set to 0.5rem calc(1.25rem + 2px) 0.5rem 0.