### CSS For a Little Kid 🌸🌈

Here I am going to teach you everything you need to know about CSS. So you can turn your blank HTML into something beautiful. I will not be covering every property or option that CSS has to offer, because there are hundreds. But I will be covering all the concepts you need to know in order to get started with CSS.



![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kh1221jwu45kypmq109r.gif)

**Let’s first get started with what CSS is:**

A common misconception is that CSS is a programming language. But that is incorrect. CSS is actually a styling language that is used for modifying the appearance of the content of web pages. Just as HTML is used for the content of web pages.CSS is used for the presentation of that content. Due to the fact that CSS is used for presentation and design. There are many ways to do the same thing. HTML on the other hand has set elements for most things. This means there is usually only one correct way to do things in HTML. The ability to do things in many different ways is the reason, most people either love or hate CSS.

I personally love it, since it lets you express your creativity and gives you the freedom to do things how you want. Now that we understand what CSS is let’s dive into the details of how to use CSS. 

First, we need to discuss the syntax of CSS.


Luckily the syntax is straightforward and easy to understand.

```
Selector{
	Property 1 :value;
	Property 2:value;
}
```


The first part of the syntax is a selector.

There are many different types and combinations of selectors, which we’ll talk about later. But for now, all you need to know is that a CSS style starts with a selector to apply the style too. Next comes an opening and closing curly brackets. That is used to denote the start and end of the styles that apply to the selector.

Everything in between these curly brackets will be styles that are applied to the HTML elements that match the selector.

Lastly inside the curly brackets, is one or more property-value pairs. Each of these pairs defines a property such as color, font size, width, etc, and a value for that property.

A basic example of the CSS syntax will be setting the text color of all h1 elements to blue.

```
h1{
	Color: blue;
 }
```

Now that we have the syntax out of the way.

Let’s focus on the various selectors.Css contains many different types of selectors but the main selectors are ‘element’, ‘class’, and ‘id’ selectors.

We have already seen the element selector in the previous example of turning all h1’s blue. Any HTML element can be used as a selector and this style is defined for that selector will apply to all HTML elements of that type. By far the most common and useful selector is the class selector.

The class selector lets you select HTML elements based on their class attribute.

A class is just an attribute that all HTML elements can have and is used with CSS to distinguish elements for specific styling.

The class attribute can also have multiple different classes in the same attribute as long as they are separated by a space.

Classes are the most common selector used because they are amazing for creating reusable components.

For example, if you have a site with three different types of buttons that all share the same basic styling but have a different color.

You can use one base class of buttons to define all the styles shared between all buttons. You can have then three other classes that define the specific color for the button.

Then all you need to do is add both the base button class and your color-specific class to your HTML button element. Here I have all the styles defined in the base button class and the color-specific class.

```
<button class =”btn btn-1”>button 1</button>
<button class =”btn btn-2”>button 2</button>
<button class =”btn btn-3”>button 3</button>
```

```
.btn{
	Padding : 10px;
	color:white;
}

 btn-1{background-color:green;}

 btn-1{background-color:blue;}

 btn-1{background-color:purple;}
```


The last comment selector is the id selector

The id selector is very similar to the class selector in that it is an HTML attribute. But an element can only have one id while it can have multiple classes. And id also should be unique across the entire web page. But HTML does not actually enforce this.

To use an id as a selector you simply need to use a pound sign followed by the id name, much like how classes use a period followed by the class name.

```
<h1 id=”main-header>Title</h1>
```

```
#id{
 property:value;
}
```

On top of having many different selectors, CSS has multiple different ways to combine selectors together to make your selectors more specific.

The first way to combine selectors is specify multiple selectors that an element must have in order to be styled. To do this, you need to write the various different selectors together with no spacing between them.

```
.selector-1.selector-2{
	property:value;
}
```

For example, if you wanted to select all h1 elements with the class large heading, then you would write the following selector.

```
<h1 class=”large-heading”>Title</h1>
```

```
h1.large-heading {
	font-size:200%;
}
```

If you wanted to select an element with the id big-blue and both the class large blue.

```
<h2 id =”big-blue” class=”large blue”>Title</h2>
```

```
#big-blue.large.blue{
	Color:blue;
	font-size:200%;
}
```

All the HTML elements can be combined in this way as many times as you want to create specific or general rules.

Another way to combine selectors is to use multiple selectors to specify an ancestor of an element. To do this you will put a space between the ancestor and child selector.

For example to select all p tags inside a div, you simply need to use the following selector.

```
<div>
	<p>Selected</p>
	<p>Selected</p>
	<span>
		<p>Selected</p>
	</span>
</div>
```


```
div p {
	Color : red;
 }
```

This will select all p tags, that have a div as their ancestor. Even if the div tag is not the direct parent of the p tag. This combination of selectors can be combined with the previous combination of selectors to 
Make even more specific selectors.

For example, to select all h1 tags, with the class of brown to have a header with the class main header as their ancestor, you would do this.

```
<header class=”main-header>
	<h1 class=”brown”>Selected</h1>
</header>
```

```
header.main-header h1.brown{
	Color: brown;
 }
```

The last common combination of selectors is when you want to share a set of style properties and values between multiple selectors.

If you have a class big and another class large, that both have the same style properties and values, then you can combine these selectors into one selector by using a comma between the selectors. This allows you to avoid duplication.



```
.big{
	font-size:200%              
}

.large{
	font-size:200%
}

.big, .large{
	font-size:200%
}
```

It is important to note that all the CSS combination selectors can be used together to create even more complex combinations if needed.

There is also one other form of selector the everything selector, that is used to select every element on the entire web page. This selector is defined as the asterisk symbol and is only used to set some defaults for your entire webpage such as font family.

```
*{
font-family: Arial;
}
```

 The last thing we need to discuss before writing some css is how to load the styles we write into our html page.

There are 3 main ways to do this. The first and by far the worst is to use inline styles. An inline style is CSS that is written directly inside an Html element and thus does not need a selector.

```
<h1 style =”color:red;”>Red Title</h1>
```

This is done through the use of the style attribute. This is a terrible idea though since HTML is meant for the content only and mixing CSS styles into the HTML elements adds presentation to the HTML file, which is meant for CSS files. It prevents us from reusing those styles anywhere else since they are written into the actual HTML element.
Lastly, depending on the styles, you use inline, your page may load slower.

The second option of using the style HTML element is slightly better but still a bad idea. 

```
<head>
	<style>
		.blue{
			Color:blue;
		}
	</style>
</head>
```

The style element is an HTML element defined in the head and formatted exactly like a CSS file. The problem with using the style element though is that the presentation of the web page is defined in the HTML file and not a CSS file. The styles you define in the style element are also only available on the page you define them and are not reusable across multiple pages.

The final and the best way to define CSS styles is to use a separate CSS file and link to it from the HTML.
All the styles for the entire webpage can be defined in one or more CSS files and they can be added to any web page by using a simple link element inside the head.

The link element is a simple element that can be used to link files to the HTML and its main use is to link CSS files. The link element is also an empty element that uses the rel attribute which stands for the relationship to define the relationship between the linked file and the HTML document. In the case of CSS, the rel attribute will be a stylesheet since CSS is a stylesheet for the HTML. 

```
<head>
<link rel=”stylesheet”  hrf=”style.css>
</head>
```

The only other attribute that we need to define is the href attribute. The href attribute works exactly the same as the href attribute of an anchor tag and should point to either your CSS file or the URL of another person’s CSS file. 

Using external CSS files like this is the best way to CSS since it separates the presentation and contents of websites and allows the reusability of styles across the website. 

Now that we have an understanding of how to write CSS styles and select specific Html elements.

```
Happy Coding !☕​🌱
```

 
