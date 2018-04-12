# Shapeshift

A flexible unintrusive CSS framework.


## Features


### flex(direction)
Defines the element as a flex element and sets the flex-direction for its children.

| param 	| value 	|
|:----------|:----------|
| direction	| row 		|
|			| col 		|




### flex(size)
Determines the flex amount for the element.

| param 	| value 	|
|:----------|:----------|
| size		| 1-10 		|


### size(fraction)
Determines the width of the element.

| param 	| value 	| description |
|:----------|:----------|:------------|
| fraction	| ex. 1/4   | This value can be any fraction between 1/10 to 1/1. A complete list of values can be found below.  | 
|			|			| 1/10, 2/10, 3/10, 4/10, 5/10, 6/10, 7/10, 8/10, 9/10 |
|			|			| 1/9, 2/9, 3/9, 4/9, 5/9, 6/9, 7/9, 8/9			   |
|			|			| 1/8, 2/8, 3/8, 4/8, 5/8, 6/8, 7/8					   |
|			|			| 1/7, 2/7, 3/7, 4/7, 5/7, 6/7						   |
|			|			| 1/6, 2/6, 3/6, 4/6, 5/6							   |
|			|			| 1/5, 2/5, 3/5, 4/5							       |
|			|			| 1/4, 2/4, 3/4									       |
|			|			| 1/3, 2/3										       |
|			|			| 1/2										       	   |
|			|			| 1/1										       	   |



### pad(size,direction)
Applies padding to all sides of an element or a specified side.

| param 	| value 	| description |
|:----------|:----------|:------------|
| size		| xs 	    | sizes are rem based  	| 
|			| sm		| 						|
|			| md		|						|
|			| lg		| 						|
|			| xl		| 						|
| direction	| 			| If this parameter is not supplied, padding will be applied to all sides of the element |
| (optional)| t			| Top					|
| 			| r			| Right					|
|			| l			| Left					|
|			| b			| Bottom				|
|			| h			| Horizontal			|
|			| v			| Vertical				|


### margin(size,direction)
Applies margin to all sides of an element or a specified side.

| param 	| value 	| description |
|:----------|:----------|:------------|
| size		| xs 	    | sizes are rem based  	| 
|			| sm		| 						|
|			| md		|						|
|			| lg		| 						|
|			| xl		| 						|
| 			| -xs 	    | negative values can also be applied | 
|			| -sm		| 						|
|			| -md		|						|
|			| -lg		| 						|
|			| -xl		| 						|
| direction	| 			| If this parameter is not supplied, padding will be applied to all sides of the element |
| (optional)| t			| Top					|
| 			| r			| Right					|
|			| l			| Left					|
|			| b			| Bottom				|
|			| h			| Horizontal			|
|			| v			| Vertical				|


### gutter(size)
Applies gap between child elements while still allowing the children to align to the parent elements horizontal bounds.

| param 	| value 	| description |
|:----------|:----------|:------------|
| size		| xs 	    | sizes are rem based  	| 
|			| sm		| 						|
|			| md		|						|
|			| lg		| 						|
|			| xl		| 						|



### align(type)
Aligns the children of a flex element.

| param 	| value 			| description |
|:----------|:------------------|:------------|
| alignment	| start 	    	| 			  | 
|			| center			| 			  |
|			| end				|			  |
|			| space-around		|			  |
|			| space-between		|			  |


### order(number)
Customizes the display order of elements. Helpful for re-arranging elements for mobile views.

| param 	| value 			| description |
|:----------|:------------------|:------------|
| number	| 1-5 	    		| Elements with lower orders will be displayed before higher ordered elements. | 


### ratio(decimal)
Sets the element to a specified aspect ratio of its parent's width. If the element has its own content, a div should be nested within the element with a class of 'content'. Content should be placed in this div.

| param 	| value 			| description |
|:----------|:------------------|:------------|
| decimal	| 0.05 - 2	 	    | Any increment of .05 between .05 and 2. A complete list of values is below: | 
|			| 					| 0.05, 0.1 0.15, 0.2, 0.25, 0.3, 0.35 0.4, 0.45, 0.5, 0.55, 0.6, 0.65, 0.7, 0.75, 0.8 0.85, 0.9, 0.95, 1 |
|			| 	 				| 1.05, 1.1 1.15, 1.2, 1.25, 1.3, 1.35 1.4, 1.45, 1.5, 1.55, 1.6, 1.65, 1.7, 1.75, 1.8 1.85, 1.9, 1.95, 2 |


### text(alignment)
Sets the text-alignment of an element.

| param 	| value 	| description |
|:----------|:----------|:------------|
| alignment	| left 	    | 			  | 
|			| center	| 			  |
|			| right		|			  |


### bg(mode)
Defines the element as a background image. Background repeating will be disabled and the background position will be defaulted to center.

| param 	| value 	| description |
|:----------|:----------|:------------|
| mode		| contain   | 			  | 
|			| cover		| 			  |


## Shifts
Breakpoints are referred to as shifts. A shift has been defined at every 100 pixels beginning at a 400 pixel window width and ending at a 1500 pixel window width.
A layout can be altered at any shift using nearly any of the features above. To alter your layout at a shift, simply add the shift prefix to your rule.

### Shift Prefix 
The shift prefix is simply the letter s followed by the shift you wish to apply divided by 100. For example, to alter a layout at a 600 pixel window width, we just need to prefix our rule with s6:

The following example would transform the element from 100% width to 50% width at a 900 pixel window width and then to a 33.33333% width at a 600 pixel window width.

ex:
class="size(1/1) s9:size(1/2) s6:size(1/3)"

#### A complete list of shift prefixes can be found below:

s4, s5, s6, s7, s8, s9, s10, s11, s12, s13, s14, s15

The concept of shifts can be applied to all features except for ratio() and bg(). The use cases for these are too minimal to justify making the library larger than it needs to be.