# CSS

## Not select
```css
.no-select {
    -webkit-user-select: none;  /* Chrome all / Safari all */
    -moz-user-select: none;     /* Firefox all */
    -ms-user-select: none;      /* IE 10+ */
    user-select: none;          /* Likely future */     
}
```

## Animation

Animated:
```css
.animated {
    animation-duration: 1s;
    animation-fill-mode: both;
}
```

Delay:
```css
.delayed_025s {
    -webkit-animation-delay: .25s;
    -moz-animation-delay: .25s;
    animation-delay: .25s;
}
```

### fadein
Usage:
```css
.fadeIn {
    -webkit-animation: fadeIn;
    animation-name: fadeIn;
}
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

### fadeinDown
Usage:
```css
.fadeInDown {
    -webkit-animation: fadeInDown;
    animation-name: fadeInDown;
}
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