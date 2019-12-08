# SASS introduction

## Local installation
```
git clone git@github.com:Karyum/sass-intro.git
cd sass-intro
npm i
npm start

```


### - Sass is a CSS preprocessor.
#### What is a preprocessor ?
- A CSS preprocessor is a scripting language that extends CSS by allowing developers to write code in one language and then compile it into CSS. Sass is perhaps the most popular preprocessor around, but other common examples include [Less](http://lesscss.org/) and [Stylus](http://stylus-lang.com/).

#### So? What is Sass ?
- Sass (Syntactically Awesome Style Sheets) is an extension of CSS that enables you to use things like variables, nested rules, inline imports and more.


## Let's see how to use Sass





#### 1) Nested syntax

```htmlmixed=
<div class="container">
    <h1 class="title">Hello World!</h1>    
    <p class="description">
        This is a description with an image 
        <img class="description-image" src=""/>
    </p>
</div>
```

```css=
.container {
    /*   Some styling here   */
}

.title {
    /*   Some styling here   */
}

.description {
    /*   Some styling here   */
}

.description-image {
    /*   Some styling here   */
}

```

> use class only for CSS not id!!


```sass=
.container {
    /*   Some styling here   */
    
    .title {
    /*   Some styling here   */
    }
    
    .description {
    /*   Some styling here   */
    
        .description-image {
        
        }
    }
}

```


#### 2) Variables

```sass=
$cool-font: Helvetica, sans-serif;
$mario-color: #FFFFFF;
$dog-color: #964b00;

.title {
    color: $mario-color;
    font-family: $cool-font;
}
```
#
### Let's see a practical use!!
#
#### 3) Import styles

```sass=
# colors.scss
$main-blue: #4287f5;
$sub-purple: #e942f5;
```

```sass=
# app.scss
@import './colors.scss';

.title {
    color: $main-blue;
}
```

#### 4) @extend

```sass=
.button {
    border: 2px solid pink;
    border-radius: 8px;
    padding: 15px;
    min-width: 150px;
}

.sales-button {
    @extend .button;
    margin-right: 20px;
}

.exit-button {
    @extend .button;
    margin-left: 20px;
}
```



## How to setup with create-react-app


- after running create-react-app and your project is built run :
```console
$ npm install node-sass --save
```

- that's it! sass is in your project, you now only need to change from `.css` files to `.scss`
