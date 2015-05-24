# Grid
A basic responsive grid. Currently under development.

## Quick Start
All you need is the `grid.css` file. In your HTML document head, include the following code. Be sure to change the `href` to where you have the grid.css file saved.
```html
<link rel="stylesheet" href="grid.css">
```

The hierarchy of elements for the grid is `grid` --> `row` --> `col-(part#)-(total#)` --> `content`
```html
<div class="grid">
    <div class="row">
        <div class="col-25-100">
        	<div class="content">
        		Content goes here.
        	</div>
        </div>
        <div class="col-50-100">
        	<div class="content">
        		Content goes here.
        	</div>
        </div>
        <div class="col-10-100">
        	<div class="content">
        		Content goes here.
        	</div>
        </div>
        <div class="col-15-100">
        	<div class="content">
        		Content goes here.
        	</div>
        </div>
    </div>
</div>
```

## Grid Element
To start the grid element, use the `grid` class.
```html
<div class="grid"></div>
```

## Rows
Inside the grid, use the `row` class to define each row.
```html
<div class="grid">
	<div class="row"></div>
</div>
```

## Columns
Each row will contain columns. The columns in each row must equal to a width of 100% which mean the parts must equal to the total in each row. Column classes start with `.col` and have the following structure:
`.col-[part]-[total]`

For example the following column is 
+ 35/100: `.col-35-100`
+ 80/100: `.col-80-100`
+ 1/3: `.col-1-3`

The current possible column totals are:
+ `100`
+ `3`
+ `6`

Below are all the current possible column classes. 
```css
.col-10-100
.col-15-100
.col-20-100
.col-25-100
.col-30-100
.col-35-100
.col-40-100
.col-45-100
.col-50-100
.col-55-100
.col-60-100
.col-65-100
.col-70-100
.col-75-100
.col-80-100
.col-85-100
.col-90-100
.col-95-100
.col-100-100

.col-1-3
.col-2-3

.col-1-6
.col-2-6
.col-3-6
.col-4-6
.col-5-6
```


Here is a complete example of a grid with 2 rows. The first row has 4 columns at equal size, and the second row has 3 columns at varying sizes. Notice how the same total column number is the same within each row.
```html
<div class="grid">
    <div class="row">
        <div class="col-25-100"><div class="content"></div></div>
        <div class="col-25-100"><div class="content"></div></div>
        <div class="col-25-100"><div class="content"></div></div>
        <div class="col-25-100"><div class="content"></div></div>
    </div>
    <div class="row">
        <div class="col-1-6"><div class="content"></div></div>
        <div class="col-3-6"><div class="content"></div></div>
        <div class="col-2-6"><div class="content"></div></div>
    </div>
</div>
```

## Content
Your content goes within each column element and must be wrapped in the `content` class.
```
<div class="content"> Your content goes here! </div>
```