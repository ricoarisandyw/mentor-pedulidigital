# HTML

## Apa itu HTML 

HTML is the standard markup language for Web pages. (w3school)

![image](https://pbs.twimg.com/media/EwlsuVSVcAIc6p2.jpg)

HTML is Skeleton.

Given example if Web was Restourant, then HTML is layouting of the building.

![denah](https://images.tokopedia.net/img/cache/500-square/product-1/2020/6/11/105054940/105054940_86bd4e02-2458-4f83-8ca1-d62ebe62f7c8_2048_2048)

## Intro HTML

HTML is also XML kind of data type.
from the Backend or API, we know that json type is like this : 

```json
{
    "garage": "model B",
    "livingRoom": {
        "style": {
             "height": "2m"    
        }
    },
    "kitchen": {
        "washingArea": {},
        "cookingArea": {}
    }
}
```

so then XML will be like this.
```xml
<house>
    <garage>model B</garage>
    <livingRoom>
        <style>
            <height>2m</height>
        </style>
    </livingRoom>
    <kitchen>
        <washingArea />
        <cookingArea />
    </kitchen>
</house>
```

from the xml above we can said the Element are : 
`<house> <garage> <livingRoom> <height> <kitchen> <washingArea> <cookingArea>`

then in HTML we just need following what element types that available on the semantic HTML list.

## Semantic HTML

Semantic HTML is Element with a meaning.

**Non Semantic :**
```html
<div>
    <span></span>
</div>
```
div and span don't have meaning. it just used for layouting.

**Semantic :**
```html
<form /> // to creating form
<header /> // to creating header (just for indexing)
<footer /> // to creating footer (just for indexing)
<table /> // to creating table
<select /> // input type select
<option /> // list of select
<b /> // bold
<i /> // italic
```
reference :
1. https://www.w3schools.com/html/html5_semantic_elements.asp
2. https://developer.mozilla.org/en-US/docs/Glossary/Semantics
3. https://developers.google.com/style/semantic-tagging

Notes : every browser usually has it own translator from HTML to Element that visible in browser. so it's very common when `<select />` in chrome and safari is different.

## Naming Element
in HTML, we just have `<div>` to be used for creating Skeleton so that we need to giving name to our body part.

we can add naming with `id` and `class`. id is so rare to be used, it purposelly to identify **one** element only.

**example from house:**
```html
<div class="house">
    <div class="livingRoom">
    </div>
    <div class="kitchen">
        <div id="washingRoom">
            <div class="dirtySpoon"></div>
            <div class="dirtySpoon"></div>
        </div>
        <div class="cookingArea">
        </div>
    </div>
</div>
```

## Example Project

I want to make this web

![](https://cdn.dribbble.com/users/2253180/screenshots/16465396/media/1c5a46dedd6773ed61437d01437d5b8d.jpg?compress=1&resize=1600x1200&vertical=top)

https://dribbble.com/shots/16465396-mobile-app-landing-page

Let's breakdown what this web has : 
- header
    - menu
    - title
    - login
    - signup
- section 1
    - group of jumbotron
        - title super big
        - small description
    - group of mobile image
        - image mobile 1
        - image mobile 2
        - image mobile 3
    - group of download button
        - app store button
        - google play button

Then let's translate it into HTML
```html
<html>
    <header>
        <div>Home</div>
        <div>About</div>
        <div>Testimonial</div>
        <div>Contact</div>
        <img alt="logo" />
        <button class="login">Login</button>
        <button class="signup">Sign Up</button>
    </header>
    <body>
        <div class="jumbotron">
            <h1>Title</h1>
            <p>small description</p>
        </div>
        <div class="mobile-images">
            <img alt="mobile-1" src="https://www.alcatelmobile.com/wp-content/uploads/2021/07/A1L-pro_560x700_Blue-1.png" />
            <img alt="mobile-2" src="https://www.alcatelmobile.com/wp-content/uploads/2021/07/A1L-pro_560x700_Blue-1.png" />
            <img alt="mobile-3" src="https://www.alcatelmobile.com/wp-content/uploads/2021/07/A1L-pro_560x700_Blue-1.png" />
        </div>
        <div class="download-button">
            <button>App Store</button>
            <button>Google Play</button>
        </div>
    </body>
</html>
```


## Project
Find a website that you want to build then create HTML skeleton from that design