## pseudo-element

```css
p::before { content: "Hello world!"; }
```

[https://developer.mozilla.org/en-US/docs/Web/CSS/%3A%3Abefore](https://developer.mozilla.org/en-US/docs/Web/CSS/%3A%3Abefore)

## animation

带-webkit-为chrome平台写法，不带为IE10写法，为兼容两种平台，一般需要分别写两次

```css
-webkit-animation: load1 1s infinite ease-in-out;
animation: load1 1s infinite ease-in-out;
```

[https://developer.mozilla.org/en-US/docs/Web/CSS/animation](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)

@-webkit-keyframes (for Chrome) 或 @keyframes (for IE10)

```css
@-webkit-keyframes load1 {
  0%,
  80%,
  100% {
    box-shadow: 0 0 #FFF;
    height: 4em;
  }
  40% {
    box-shadow: 0 -2em #ffffff;
    height: 5em;
  }
}
```

[https://developer.mozilla.org/en-US/docs/Web/CSS/%40keyframes](https://developer.mozilla.org/en-US/docs/Web/CSS/%40keyframes)