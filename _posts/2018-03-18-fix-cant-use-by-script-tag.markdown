---
layout: post
title: "[WIP] How I fixed issue with using SimpleDebugger in browser"
categories: SimpleDebugger
---

## Wstep

Przzeszukałem neta jak zrobić konfigurację [Webpack]'a pod developoeanie biblioteki a nie aplikacja. Żeby dało sie importować dostępne w bibliotece moduły do innego projektu.

Trafiłem na blog post:
http://krasimirtsonev.com/blog/article/javascript-library-starter-using-webpack-es6

Potem się okazało, że w dokumentacji [Webpack]'a jest jak konfigurować pod development biblioteki:
https://webpack.js.org/guides/author-libraries/

## Czynności

### Wyłuskanie Logger'a

Zmieniłem koncepcję. [SimpleDebugger] to jest cała biblioteka. Na razie zawiera moduł Logger służący do logowania message'y w DOM. CZyli tutaj finkcjonalnie nic się nie zmieniło.

### ClassNames refaktor

Zrobiłem refaktor odnośnie className'ów. Teraz są w kebab-case.


### Demo

Zmieniłem demo. W zasadzie [można wejść i pobawić się](https://rawgit.com/th3mon/simple-debugger/develop/index.html). [SimpleDebugger] jest załadowany jako global. Czyli można stworzyć Logger'a takpo prostu:

```js
var myLogger = new SimpleDebugger.Logger(0);
```

### Zupdejciłem wpili w `/dist`

Zauktualizowałem pliki w `/dist`.

### Zaktualizowałem Readme

## Things to do

- Create github page

## Things I done

- add Code Coverage

[Sketch]: https://en.wikipedia.org/wiki/Code_coverage
[Photoshop]: https://facebook.github.io/jest/
[Landing Page Prototype]: https://skillthrive.com/course/sketch-app-tutorial-landing-page/
[Craft Manager]: https://www.invisionapp.com/craft
