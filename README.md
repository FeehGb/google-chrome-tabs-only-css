# google-chrome-tabs-only-css

This project is clone of google chrome tabs used only CSS

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

To use you will only need donwload the style.css and fallow these tips:


### How to use

-- After put the style.css in your directory and import in the page that you want to use you will need put in your HTML file these follows lines

How to import
```html
    <link rel='stylesheet' href='./style.css' />
```

-- To Start
```html
<div grid class="group-tabs"></div>
```
Each tab there are 3 main lines and need to fallow the sequence to work fine

1º )
```
The input has five main attribute 
    - tab  - The global style's tabs          * needs to be the same in all inputs
    - hide - used to hide the input tag       * needs to be the same in all inputs
    - type - To define the type of tag        * needs to be the same in all inputs
    - id   - id to identification the tag     * needs to be unique
    - name - name of group tab                * needs to be unique each tabs group
```
 
```html 
<input tab hide="hide" type="radio"  id="rTab-1" name="tab"> 
```


2º )
The label has 2 main attribute
    - grid-label  - The global style's label          * needs to be the same in all inputs
    - for         - To link the label and input       * needs to be the same of your linkage input
    
- Inside of label you will need to put a span tag to work the shadow in the label - 

```html
    <label class='grid-label' for='rTab-1'><span>Tab 1</span></label>
```


  
3º )
```
The div has 1 main attribute
    - tab-conten  - The global style's label          * needs to be the same in all divs
```

```html 
<div flex class="tab-content">
    Content of tabs
</div>
```


- Full example with two tabs
```html
    <div grid class="group-tabs">
        <!-- START GRID TAB 001 -->
        <input hide="hide" type="radio" tab id="rTab-1" name="tab1" checked="checked">
        <label class='grid-label' for='rTab-1'>
            <span>Tab 01</span>
        </label>
        <div flex class="tab-content">
            Content's tab 001
        </div>
        <!-- END GRID TAB 001 -->
        
        
        <!-- START GRID TAB 002 -->
        <input hide="hide" type="radio" tab id="rTab-2" name="tab1">
        <label class='grid-label' for='rTab-2'>
            <span>Tab 01</span>
        </label>
        <div flex class="tab-content">
            Content's tab 002
        </div>
        <!-- END GRID TAB 002 -->
    </div>
   
```

### To use Dark theme

You only need to put the dark atribuite in main div
```html
    <div dark grid class="group-tabs">
```

### To make the tabs responsive
You only need to put the responsive atribuite in main div
```html
    <div responsive grid class="group-tabs">
```

### To set icon

There are two ways to set icons on tab - 

1º) with text *default
- I recomend use only svg files
```html
<label class='grid-label' for='rTab-15'>
    <div icon>
        you need to put your svg here
    </div>
    <span>text beside the icon</span>
</label>
```

2º) with icon only 
*Do not use the span tag

```html
<label class='grid-label' for='rTab-15'>
    <div icon icon-only>
        you need to put your svg here
    </div>
</label>
```

### To set the number's tabs
I do not recommend to do this  ten tabs is enouth to work, but if you want you can
You will need to change style.css file

First you need to change in :root vars

1º) --tabs-amount : 10; <-- number's tabs ->
2º) You will need to find "10" in every single css declaration - unfortunately I could not put it in a variable
example:
    change
    ```css
        .group-tabs [tab]:not(:checked):nth-of-type(10n+1) + label.grid-label::after
    ```
     to
    ```css
        .group-tabs [tab]:not(:checked):nth-of-type("newNumber"n+1) + label.grid-label::after
    ```


## Built With

* [HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML) - HyperText Markup Language
* [CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS) - Cascading Style Sheets




## Versioning

1.0.0

## Authors

* **Felipe Basilio** - *Initial work* - [FeehGb](https://github.com/FeehGb)


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Inspiration
    Google Chrome
