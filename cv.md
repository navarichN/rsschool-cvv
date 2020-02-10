# Anastasia Navarich
    Mobile: +375 44 721 24 06
    Telegram: @navarich
    E-mail: navarichanastasia@gmail.com

 
##  Summary:
### I am a rational person, who likes to optimize her activities and life. I also like to learn new things and to feel how my brain works. I wanted to belong to a group of smart, interesting people who create the future. So I decided to become a programmer. 

### In the beginning it was very difficult, but I didn't give up. My enthusiasm and endurance keep to grow, because when you cannot complete a task, try to do it again and again, and when you come to an answer, you experience incredible delight! Seretonin strike in your brain and you become addicted to it.

### And, in the end, when I started to study programming, I realized that in this area I can reveal my personality, apply and improve my inclinations and, in general, be myself and feel happy.
##  Education:
   +    [Teach Me Skills](https://teachmeskills.by/kursy-programmirovaniya/frontend-html-css-javascript-minsk) - **Frontend Development** / offline
   +    [HTMLAcademy](https://htmlacademy.ru/profile/id887467) - **Frontend Development** / online
   +    [WebForMySelf](https://webformyself.com/vuejs/?utm_medium=systema&utm_source=nashikursi&utm_campaign=vue) - **Vue** / online
   +    [CodeAcademy](https://www.codecademy.com/profiles/0506832725) - **Html,Css** / online

##  Experience:

### I was lucky to have internship in [LEXX Trading Platform](https://lexxtg.com). At that time I first tried to work with Git, namely [GitLab](https://gitlab.com/navarichanastasia), because this team uses it. Also I saw the structure of a large project on **Vue.js**, how the work was organized on it and this formed my idea of ​​what else I need to learn.

##  Skills:
+   Markup: **HTML5**, **Pug**
+   Style: **CSS**, **Sass**
+   Framework: **Vue.js**
+   Tools: **Figma**, **VS Code**, **Git**
+   Methodology: **BEM**

##  Code examples:
```Sass
.list-excellence
    +df 
    +fdc
    justify-content: flex-start
    align-items: center
    margin-top: 80px
    width: 1084px
    height: 327px
    +h560
        margin-top: 0
    &__list
        +df
        +fdc
        flex-wrap: wrap
        width: 1062px
        height: 200px
        margin-top: 30px
    &__item
        display: inline-flex
        width: 516px
        height: 52px
        font-family: Roboto Slab
        font-style: normal
        font-weight: normal
        font-size: 24px
        line-height: 32px
        color: #FFFCFC
        &:before
            content: "★"
            width: 40px
            height: 40px
```
<hr>

```Pug 
<template lang = "pug">
    div.container.pt-2
        .form-group
        label(for = "name")
            | Car name
        input.form-control(type = "text" id = "name" v-model.trim = "carName")

        .form-group
        label(for = "year")
            | Car year
        input.form-control(type = "text" id = "year" v-model.number = "carYear")

        button.btn.btn-success(@click = "createCar")
        | Create car

        button.btn.btn-primary(@click = "loadCars")
        | Load cars

        hr

        ul.list-group
        li.list-group-item(v-for = "car of cars" :key = "car.id")
            strong
            | {{ car.name }} 
            | {{ car.year }}
</template> 
```


<hr>


```html
       <section id = "stocks" class = "stocks section3">
            <h3 class = "title">Внимание, АКЦИЯ!</h3>
           <div class = "wrapper">
                <div class = "stocks-slider">
                    <div class = "stocks-slider__head">
                        <p class = "stocks-slider__description">Скидка на груминг 20% до 21 апреля</p>
                    </div>
                    <span class = "exp-string">До конца акции осталось:</span>
                    <div class = "stocks-slider__time">
                        <div class = "stocks-slider__item stocks-slider__item_day">
                            <span>12</span>
                            <hr>
                            <span>день</span>
                        </div>
                        <div class = "stocks-slider__item stocks-slider__item_hour">
                            <span>12</span>
                            <hr>
                            <span>день</span>
                        </div>
                        <div class = "stocks-slider__item stocks-slider__item_minute">
                            <span>12</span>
                            <hr>
                            <span>день</span>
                        </div>
                    </div>
                </div>
                <form class = "back-call stocks-back-call">
                        <h3 class = "back-call__title">Закажите обратный звонок</h3>
                        <input type = "text" class = "back-call__input back-call__input_name" placeholder="Порода и имя">
                        <input type = "tel" class = "back-call__input back-call__input_tel" placeholder="Номер телефона">
                        <input name = "submit" type = "submit" class = "back-call__input back-call__input_btn" value = "Заказать">
                </form>

           </div>
       </section> 
```


<hr>



```JavaScript
let pageServWrap = pageServises.querySelector('.serv-wrapper');
let btnBlock = pageServises.querySelector('.servises__btn-block');
let btnCatImage = pageServises.querySelector('.servises__btn-block_cats');
let btnCatString = pageServises.querySelector('.servises__caption_cats');
let btnDogImage = pageServises.querySelector('.servises__btn-block_dogs');
let btnDogString = pageServises.querySelector('.servises__caption_dogs');

function showServisesForCats() {
    btnDogString.remove();

    let blockServList = document.createElement('div');

    blockServList.className = "serv-list serv-list_cats";
    blockServList.insertAdjacentHTML('afterbegin', '<div class = "serv-list__wrapper"><ul class = "serv-list__item"><span>Груминг</span></ul><ul class = "serv-list__item"><span>Магазин</span></ul><ul class = "serv-list__item"><span>Маникюр</span></ul><ul class = "serv-list__item"><span>Дрессировка</span></ul><ul class = "serv-list__item"><span>Магазин</span></ul><ul class = "serv-list__item"><span>Массаж</span></ul></div>');
    
    let newCatBtnBlock = document.createElement('div');
    
    newCatBtnBlock.className = "servises__btn-block-on";
    newCatBtnBlock.insertAdjacentHTML('afterbegin', '<img src = "styles/img/bbb.png" class = "servises__btn-block-on_cats"></img>');
    
    btnDogImage.replaceWith(blockServList);
    btnBlock.replaceWith(newCatBtnBlock);

    setTimeout(blockServList.classList.add('appearance-on-the-right'), 10000);
}

function showServisesForDogs() {
    btnCatString.remove();
    btnDogString.remove();

    let blockServList = document.createElement('div');

    blockServList.className = "serv-list serv-list_dogs";
    blockServList.insertAdjacentHTML('afterbegin', '<div class = "serv-list__wrapper"><ul class = "serv-list__item"><span>Груминг</span></ul><ul class = "serv-list__item"><span>Магазин</span></ul><ul class = "serv-list__item"><span>Маникюр</span></ul><ul class = "serv-list__item"><span>Дрессировка</span></ul><ul class = "serv-list__item"><span>Магазин</span></ul><ul class = "serv-list__item"><span>Массаж</span></ul></div>');

    let newDogBtnBlock = document.createElement('div');

    newDogBtnBlock.className = "servises__btn-block-on";
    newDogBtnBlock.insertAdjacentHTML('afterbegin', '<img src = "styles/img/druk.png" class = "servises__btn-block-on_dogs"></img>');

    btnCatImage.replaceWith(blockServList);
    btnDogImage.replaceWith(newDogBtnBlock);

    setTimeout(blockServList.classList.add('appearance-on-the-left'), 10000);
}

btnCatImage.addEventListener('click', showServisesForCats);
btnDogImage.addEventListener('click', showServisesForDogs);
```
##  English:
+   ### I learn English at shool [Intarnational House](https://www.ih.by). My level **Pre-Intermideate(A2)**
+   ### Also i use an app called [Simpler](https://play.google.com/store/apps/details?id=ru.zengalt.simpler&hl=ru)
+   ### And I watch movies with  English subtitles


##  Polish:
+   ### I learn Polish myself and with a mentor online. My level **A1**
