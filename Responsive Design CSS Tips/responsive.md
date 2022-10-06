# Responsive Design CSS Tips

**Padding/Margin**

We usually use a lot of padding when we make websites for desktops, to make them more attractive.While making it responsive for mobiles,tables try decresing the existing paddings and margins.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/pzvsnmso5rh9ph4rncxw.jpeg)

**User em/rem/percentage**

Always try using em/percentage/rem instead of px, so that the text, images size adjust with respect to the device width.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8u4i3xqlnp9l14gvi15m.jpeg)


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/d22vhf2kfz55eukzw2wu.jpg)

**Flex-wrap**

Using flexbox to align the HTML elements such as <`div>,<p>` etc provides the force elements onto one line or can wrap onto multiple lines according to their width.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/v89o63x69850590hxuy1.png)

**Media Query**

Media query should be used to set width and height according to the breakpoints. Breakpoint refers to the width the website starts looking distortd.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fytn7pog028s84cpna24.png)

**Box-Sizing**

It resolves a lot of problems padding causes, using box-sizing on HTML elements with a percentage width will take padding into account rather than having to adjust the width due to padding.

`{box-sizing : border box;}`


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/aryucfhf5eao222by5wv.png)

Did you find it useful?
Get in touch for more!
