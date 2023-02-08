# Документация для frontend разработчиков
## 1. [BEM](https://ru.bem.info/methodology/)
    При верстке используем смешаный формат стилей именования Two Dashes и CamelCase, например,
```html
        <b>bigBlock__bigElement--bigModificator</b>
```
    Ниже приведены рекомандации для блоков, которые чаще всего есть на любом сайте, которые необоходимо придерживаться.

**Базовый каркас для верстки** 
```html
<div class="wrapper">
        <header class="header"></header>
        <main class="main">
            <b>Дополнительные обертки добавляются строго в этой области (Пример ниже)</b>
        </main>
        <footer class="footer"></footer>
</div>
```
**Базовый каркас для внутренних страниц**
```html
    <div class="wrapper">
        <header class="header"></header>
        <main class="main">
            <div class="insidePage">
                <div class="insidePage__sidebar insidePage__sidebar--left"></div>
                <div class="insidePage__mainContent">
                    Основная рабочая область
                </div>
                <div class="insidePage__sidebar insidePage__sidebar--right"></div>
            </div>
        </main>
        <footer class="footer"></footer>
    </div>
```
**Хлебные крошки** 
```html
<nav class="breadcrumb" aria-label="Breadcrumb">
  <ul class="breadcrumb__list">
    <li class="breadcrumb__item"><a class="breadcrumb__link" href="#">Home</a></li>
    <li class="breadcrumb__item"><a class="breadcrumb__link" href="#">About</a></li>
    <li class="breadcrumb__item"><a class="breadcrumb__link breadcrumb__link--last" href="#" aria-current="location">Vision</a></li>
  </ul>
</nav>
 Или
<div class="breadcrumb" aria-label="Breadcrumb">
    <div class="breadcrumb__container container">
        <nav class="breadcrumb__nav">
            <ul class="breadcrumb__list">
                <li class="breadcrumb__item"><a class="breadcrumb__link" href="#">Home</a></li>
                <li class="breadcrumb__item"><a class="breadcrumb__link" href="#">About</a></li>
                <li class="breadcrumb__item"><a class="breadcrumb__link breadcrumb__link--last" href="#" aria-current="location">Vision</a></li>
              </ul>
        </nav>
    </div>
</div>
```
**Кнопки** 
В зависимости от сложности макетов испольузются такие модификаторы как
--size
--color
```html
<a href="#" class="button button--red button--sizeBig">
  <span class="button__prependIcon">
     🚀
  </span>
  <span class="button__text">Текст ссылки или кнопки</span>
  <span class="button__appendIcon">
     👨‍🚀
  </span>
</a>
```

**Превью карточки товара** 
```html
<div class="previewItem">
    <div class="previewItem__imageContainer">
        <picture class="previewItem__picture">
            <img src="src" alt="" class="previewItem__image">
        </picture>
    </div>
    <div class="previewItem__body">
        <div class="previewItem__name"></div>
        <div class="previewItem__desc"></div>
        <a href="#" class="previewItem__button button"></a>
    </div>
  </div>
  ```
  **Пример тизеров** 
```html
    <div class="tizers">
        <div class="tizers__container container">
            <div class="tizers__row row">
                <div class="tizers__itemContainer tizers__itemContainer--w33">
                    <div class="tizersItem">
                        <div class="tizersItem__iconContainer">
                            <img src="icon" alt="" class="tizersItem__icon">
                        </div>
                        <div class="tizersItem__desc">

                        </div>
                    </div>
                </div>
                <div class="tizers__itemContainer tizers__itemContainer--w33">
                    <div class="tizersItem">
                        <div class="tizersItem__iconContainer">
                            <img src="icon" alt="" class="tizersItem__icon">
                        </div>
                        <div class="tizersItem__desc">
                            
                        </div>
                    </div>
                </div>
                <div class="tizers__itemContainer tizers__itemContainer--w33">
                    <div class="tizersItem">
                        <div class="tizersItem__iconContainer">
                            <img src="icon" alt="" class="tizersItem__icon">
                        </div>
                        <div class="tizersItem__desc">
                            
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
```

**Детальная карточка товара** 


```html
    <div class="cardProduct">
        <div class="cardProduct__row">
            <div class="cardProduct__sideBar">
                <div class="cardProduct__gallery gallery">
                    <div class="gallery__sliderContainer">
                        <div class="gallery__slide">
                            <a href="#" data-fancybox class="gallery__link">
                                <picture class="gallery__picture">
                                    <img class="gallery__image" src="src" alt="">
                                </picture>
                            </a>
                        </div>
                        <div class="gallery__slide">
                            <a href="#" data-fancybox class="gallery__link">
                                <picture class="gallery__picture">
                                    <img class="gallery__image" src="src" alt="">
                                </picture>
                            </a>
                        </div>
                        <div class="gallery__slide">
                            <a href="#" data-fancybox class="gallery__link">
                                <picture class="gallery__picture">
                                    <img class="gallery__image" src="src" alt="">
                                </picture>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="cardProduct__content">
                <div class="cardProduct__rating rating"></div>
                <div class="cardProduct__title"></div>
                <div class="cardProduct__desc"></div>
                <button class="cardProduct__button button--addToCart"></button>
            </div>
        </div>
    </div>
```

**Чекбокс или радиокнопка** 
```html
    <label class="checkbox">
        <input class="checkbox__input" type="checkbox" id="MyCustomCheckbox">
        <svg class="checkbox__icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 22 22">
          <rect width="21" height="21" x=".5" y=".5" fill="#FFF" stroke="#006F94" rx="3" />
          <path class="tick" stroke="#6EA340" fill="none" stroke-linecap="round" stroke-width="4" d="M4 10l5 5 9-9"></path>
        </svg>
        <span class="checkbox__label">Описание</span>
    </label>
```

## 2. Стек плагинов

* [Слайдер - swiper.js](https://swiperjs.com/)
* [Маска в инпуты](https://imask.js.org/)
* [Анимация GSAP](https://greensock.com/gsap/)
* [Тригер на скролл для анимации GSAP (Если требуется анимация плавающих элементов на мобильных устройствах)](https://scrollmagic.io/)
* [Умный скролл для мобильных устройств, необходимый для более плавной анимации](https://github.com/cubiq/iscroll)
