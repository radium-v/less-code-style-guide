# Less Code Style Guidelines

## Values and Variables

Rems are the best  
Unless they really don't work.  
Use what makes the most sense.  

```less
font-size: 1rem; // 16px
```

## Structure

Selector, then space.  
Then curly brace and new line.  
Solo closing brace.  

```less
.hooray {
	text-align: center;
}
```


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

## Selectors

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
