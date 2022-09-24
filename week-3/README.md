# IDE + Element

IDE is a tools for coding

here are some IDE tools : 
1. VSCode
2. Vim
3. NeoVIM
4. Sublime
5. Atom


There are also online IDE : 
1. CodePEN
2. JSFiddle

Pick your IDE, if you have high spec computer then you can install IDE but if not then you can use CodePen or JSFiddle.

# Linting

Linting is neating the code so that we can read easily the code. example : 
```html
<div> <span>HelloWorld</span>  </div>
```
After lint : 
```html
<div>
    <span>HelloWorld</span>
</div>
```

linting is very usefull for developing project.

# Run & Inspect your HTML

## Run

to run you HTML File, you just need to double click your html files then it will open browser for you to running.

## Inspect

modern browser like Chrome, Safari, Firefox will have tools to "inspect" our HTML Page. 

we can check which code represent specific content in our page with :
1. Right Click select Inspect on the element.
2. On the right side you will see the DevTools Panel.
3. See the representative of selected ui on DevTools element viewer.

# Little using DevTools

an old way to direct check our web change is using dev tools, we use this way before

# Style

Style is clothes of our website. here are style structure : 

![](https://assets.digitalocean.com/articles/how-to-build-a-website-with-css/css-diagram.png)
*source : digitalocean*

selector is element finder. 

example : input, .form-control, #main-logo
properties is what we can change in those element.
example : color, display, position
value has different collection depend on the properties. example : 1px, blue, auto, flex.


### Selector Type : 
style without anything mean it for tag. example : `<input />`
style with (.) at the beginning mean it for class. example :
`<div class="bg-red" />`
style with (#) at the beginning mean it for id.
example :
`<div id="bg-red" />`

## Creating Style inside HTML

one technique to creating clothes for our html is using style which coded inside our HTML files. below `<html>` code this code : 
```html
<head>
    <style>
    /* we will create style in here */
    </style>
</head>
```

then inside style we can create our clothes. given example we will create red clothes. then we can code this inside `<style />`

```css
.bg-red {
    background: red;
}
```

Final Result : 

```html
<head>
    <style>
    /* we will create style in here */
    .bg-red {
        background: red;
    }
    </style>
</head>
```

## Put it in our body part

wait, we are not creating the body part which we will giving those color. let's create it. or if you already have skeleton then you can giving color to our body part.

```
<html>
    <head>
        <style>
        /* we will create style in here */
        .bg-red {
            background: red;
        }
        </style>
    </head>
    <body>
        <div class="bg-red"></div>
    </body>
</html>
```

oh no, why we don't see anything? because your body part is don't have anything inside it. we can put simple word inside it. 

```
<html>
    <head>
        <style>
        /* we will create style in here */
        .bg-red {
            background: red;
        }
        </style>
    </head>
    <body>
        <div class="bg-red">I'M RED</div>
    </body>
</html>
```

Great, you know should see I'M RED with background red.

# Let's try coloring our website from Week-2

```html
<html>

<head>
    <style>
        body {
            background: #1E5BFA;
        }

        .menu {
            color: white;
        }

        .login {
            color: white;
            background: none;
            border: none;
        }

        .signup {
            background: white;
            color: black;
            border: none;
        }

        /* Trick to give white color to all child of jumbotron class */
        .jumbotron {
            color: white;
        }

        /* this style is for class="download-button" child with selector <button>  */
        .download-button button {
            color: white;
            background: black;
            border: none;
        }

    </style>
</head>

<body>
    <header>
        <div class="menu">Home</div>
        <div class="menu">About</div>
        <div class="menu">Testimonial</div>
        <div class="menu">Contact</div>
        <img alt="logo" src="https://cdn-icons-png.flaticon.com/512/174/174880.png" />
        <button class="login">Login</button>
        <button class="signup">Sign Up</button>
    </header>
    <div class="jumbotron">
        <h1>Smart Home Application</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tenetur corrupti deserunt accusantium nostrum ratione magni dicta explicabo. Cupiditate assumenda sequi sunt saepe, laboriosam dolorum repellat error quas. Delectus, culpa dicta!</p>
    </div>
    <div class="mobile-images">
        <img alt="mobile-1" src="https://www.alcatelmobile.com/wp-content/uploads/2021/07/A1L-pro_560x700_Blue-1.png" />
        <img alt="mobile-2" src="https://www.alcatelmobile.com/wp-content/uploads/2021/07/A1L-pro_560x700_Blue-1.png" />
        <img alt="mobile-3" src="https://www.alcatelmobile.com/wp-content/uploads/2021/07/A1L-pro_560x700_Blue-1.png" />
    </div>
    <div class="download-button">
        <button>Download on the App Store</button>
        <button>GET IT ON Google Play</button>
    </div>
</body>

</html>
```


## Creating File Style

to creating style, we can create file called. `index.css`

then we can move style from `<style>` tag in those file : 
```css
/* index.css */
.bg-red {
    background: red;
}
```

then import it inside our html file.
```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```