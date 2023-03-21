# Responsive web design

- Your application should look good on every device (mobile, tablet, laptop, ...)  
- Actually the device isn't the important factor, what matters is the size of the screen - the viewport size

## Mobile first approach 

- Instead of designing the app for a large screen first and then adapting it to a smaller screen it is a better strategy to implement the small screen version first and then expand it to the larger screen  
- You concentrate on the essential functionality first, exactly as in the MVP (Minimum viable product) principle  

## Media queries

- We achieve responsiveness via media queries that set break points where according to the screen size the styling changes

Nice list for screen sizes and media queries can be found here: 
https://gist.github.com/gokulkrishh/242e68d1ee94ad05f488

This styling is applied for any device with a width up to 480px:  

```
@media (max-width: 480px) {
	.container {
		width: 100vw;
	}

	.content {
		width: 50%;
	}
}
```

## Font size

- Set a default font size for the html (16px is a recommended font size)

```
  html {
    font-size: 16px;
  }
```

- And from that point on use **rem** (relative to the html font size) (e.g. 2rem = 32px)
- Or easier to calculate: html { font-size: 10px } => 1.6rem = 16px  
- If for some reason you want to define the size relative to the parent use **em**