# Less Code Style Guidelines

## Values and Variables

Rems are the best  
[Unless they really don't work.](http://fvsch.com/code/bugs/rem-mediaquery/)  
Use what makes the most sense.  

```less
font-size: 1rem; // 16px
```

-

### Structure

Selector, then space.  
Then curly brace and new line.  
Solo closing brace.  

```less
.hooray {
}
```

-

### Indentation

Use tabs to indent.  
Only one tab per level.  
Retract closing brace.

```less
.nope {
	text-align: center;
}
```

-

### Mulitple Selectors

Commas with newlines  
Split multiple selectors.  
Alphabetically.  

```less
.george,
.john,
.paul,
.ringo {
	text-align: center;
}
```

-

### Properties

Extends always first.  
All mixins go after that.  
Then the properties.

```less
.fancy-class {
	&:extend(.super);
	.story(@bro: 1rem);

	border: none;
	text-align: center;
}
```

-

### Nested Selectors

Nested selectors  
Have a comment afterwards.  
Search is now easy.

Visibility  
Prevents ridiculousness  
And over-nesting.  

```less
.parent {

	.child { // .parent .child

		&:hover { // .parent .child:hover

			> .woah { // .parent .child:hover > .woah

				&:nth-of-type(2n + 1) { // .parent .child:hover > .woah:nth-of-type(2n + 1)
					text-align: center;
				}
			}
		}
	}
}
```

-

### Selectors

Classes are the best.  
Please use IDs sparingly.  
Stop, don't qualify.  

```less
#bad {
	// stuff
}

ul.be-sorry {
	// over-qualified
}

```

-

### Media Queries

Store queries as strings.  
Declare variables.  
CSS cascades.

```less
@tablet-up: ~"screen and (min-width: 768px)";
```


Media queries  
Nested inside the module.  
Mobile First, of course.

```less
.box {
	width: 1rem;
	
	@media @tablet-up {
		width: 2rem;
	}
}
```
