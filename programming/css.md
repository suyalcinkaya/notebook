# CSS

## Reset & Make Fonts Look Better
```css
* {
    font-weight: normal;
    -webkit-font-smoothing: antialiased !important;
    -moz-font-smoothing: antialiased !important;
    -moz-osx-font-smoothing: grayscale;
    speak: none;
    font-style: normal;
    font-weight: normal;
    font-variant: normal;
    text-transform: none;
    line-height: 1;
    -webkit-font-smoothing: antialiased;
}
```

## no-select
```css
-webkit-user-select: none;      /* Chrome all / Safari all */
-moz-user-select: none;         /* Firefox all */
-ms-user-select: none;          /* IE 10+ */
user-select: none;              /* Likely future */  
```

## Centering with grid
Html
```html
<span>I'm centered!</span>
```

Css
```css
body, html {
  height: 100%;
  display: grid;
}

span {
  margin: auto;
}
```

## fadeIn animation
Usage:
```css
animation-duration: 1s;
animation-fill-mode: both;
-webkit-animation: fadeIn;
animation-name: fadeIn;
```

Definition:
```css
@keyframes fadeIn {
    from {
        opacity: 0;
    }
    
    to {
        opacity: 1;
    }
}
```

## fadeInDown animation
Usage:
```css
animation-duration: 1s;
animation-fill-mode: both;
-webkit-animation: fadeInDown;
animation-name: fadeInDown;
```

Definition:
```css
@keyframes fadeInDown {
    from {
        opacity: 0;
        transform: translate3d(0, -100%, 0);
    }
    
    to {
        opacity: 1;
        transform: none;
    }
}
```

## Animation delay
Delay for 0.25 seconds;
```css
-webkit-animation-delay: .25s;
-moz-animation-delay: .25s;
animation-delay: .25s;
```

## Hover effect
```css
box-shadow: 0 5px 10px 0 rgba(69, 129, 208, 0.12);
```

## Transition effect
```css
-webkit-transition: 0.3s;
transition: 0.3s;
```

## Transition slide-in
Usage:
```css
-webkit-animation: 3s slide-in 0.5s forwards;
animation: 3s slide-in 0.5s forwards;
```

Definition:
```css
@-webkit-keyframes slide-in {
  0% {
    opacity: 0;
    -webkit-transform: translateY(104px);
    transform: translateY(104px); 
  }
  100% {
    opacity: 1;
    -webkit-transform: translateY(0px);
    transform: translateY(0px); 
  } 
}

@keyframes slide-in {
  0% {
    opacity: 0;
    -webkit-transform: translateY(104px);
    transform: translateY(104px); 
  }
  100% {
    opacity: 1;
    -webkit-transform: translateY(0px);
    transform: translateY(0px); 
  } 
}
```





## font-face
Usage:
```css
font-family: 'Font', sans-serif;
```

Definition:
```css
@font-face {
    font-family: 'Font';
    src: url('../fonts/font_regular.woff2') format('woff2'), /* Super Modern Browsers */
        url('../fonts/font_regular.woff') format('woff'), /* Pretty Modern Browsers */
        url('../fonts/font_regular.ttf') format('truetype'); /* Safari, Android, iOS */
    font-weight: 400;
    font-style: normal;
}
```

## List of CSS Frameworks
- [Bulma](https://bulma.io/)
- [Milligram](https://milligram.io/)
- [Semantic UI](https://semantic-ui.com/)
- [Bootstrap](https://getbootstrap.com/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Tachyons](https://tachyons.io/)
- [The Admin](http://thetheme.io/theadmin/)
- [Animate.css](https://daneden.github.io/animate.css/)
