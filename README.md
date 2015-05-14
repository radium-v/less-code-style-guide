# Less Code Style Guidelines

## Values and Variables

* * *

> Rems should be the best  
> Unless they really don't work.  
> Use what makes most sense.

>     font-size: 1rem; // 16px

## Structure

* * *

> Selector, then space.  
> Then curly brace and new line.  
> Solo closing brace.

> 	.hooray {
> 		text-align: center;
> 	}

* * *

> Commas with newlines  
> Split multiple selectors.  
> Alphabetical.

> 	.george,
> 	.john,
> 	.paul,
> 	.ringo {
> 		text-align: center;
> 	}

* * *

> Extends always first.  
> All mixins go after that.  
> Then the properties.

> 	.fancy-class {
> 		&:extend(.super);
> 		story(@bro: 1rem);
> 	
> 		border: none;
> 		text-align: center;
> 	}

* * *


> Nested selectors  
> With a comment afterwards.  
> Search is now easy.

> Visibility  
> Prevents ridiculousness  
> And over-nesting.  

> 		.parent {
> 			
> 			.child { // .parent .child
> 				
> 				&:hover { // .parent .child:hover
> 					
> 					> .woah { // .parent .child:hover > .woah
> 						
> 						&:nth-of-type(2n + 1) { // .parent .child:hover > .woah:nth-of-type(2n + 1)
> 							text-align: center;
> 						}
> 					}
> 				}
> 			}
> 		}

## Selectors

* * *

> Classes are the best.  
> Please use IDs sparingly.  
> Stop, don't qualify.  

> 	#bad {
> 		// stuff
> 	}

## Indentation

> Use tabs to indent.  
> Only one tab per level.  
> Retract closing brace.  

> 	.nope {
> 		text-align: center;
> 	}
