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
- [The Admin](http://thetheme.io/theadmin/)
- [Semantic UI](https://semantic-ui.com/)
- [Bootstrap](https://getbootstrap.com/)
- [Animate.css](https://daneden.github.io/animate.css/)
