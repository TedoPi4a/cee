<section><h1 style="text-align: center; font-size: clamp(2.4rem, 8vw, 4rem);">Ръководство</h1>
    <main>
        <div class="div1">
            <img src="/people/Emil_Taskov.jpg" alt="">
            <h2>Емил Тасков</h2>
            <h4>Председател на УС</h4>
           <p> В 1973 год. завършва ВИСИ София, специалност "Промишлено и гражданско строителство" </p></div>
        <span>
            <div class="parent">
           
                <div class="div2">
                    <img src="/people/Nikola_Dukov.jpg" alt="">
                    <h2>Никола Дуков</h2>
                    <h4>Заместник-председател</h4>
                    <p>От 2007 г. до 2011 г. е изпълнителен директор на фирма „Газ Флоу Контрол“ АД.</p>
                </div>
                
                <div class="div3">
                    <img src="/people/Cvyatko_Shokov.jpg" alt="">
                    <h2>Цвятко Шоков</h2>
                    <h4>Заместник-председател</h4>
                    <p>Мениджър с особено активно участие в обследвания за енергийна ефективност на сгради и сертифициране на сгради и със значителен административен опит.</p>
                </div>
                
                <div class="div4">
                    <img src="/people/Natalia_Sabeva.jpg" alt="">
                    <h2>Наталия Събева</h2>
                    <h4>Изпълнителен Секретар</h4>
                    <p>Представляваща "Контач" ООД, гр.Съединение, мениджър с особено активно участие в обследвания за енергийна ефективност на сгради и сертифициране на сгради.</p>
                </div>
                
                <div class="div5">
                    <img src="/people/Sevdalina_Dzhabarska.jpg" alt="">
                    <h2>Севдалина Джабарска</h2>
                    <h4>Член на УС</h4>
                    <p>Първия председател на УС на Камара за енергийна ефективност понастоящем Камара на енергийните одитори. Управител е на „Енерджи Сейвинг”ЕАД.</p>
                </div>
                
                <div class="div6">
                    <img src="/people/Kostadin_Arnaudov.jpg" alt="">
                    <h2>Инж. Костадин Арнаудов</h2>
                    <h4>Член на УС</h4>
                    <p>Управител на "Аркас" ООД, гр.Пловдив, със значителен професионален опит, един от първите експерти в България, придобил квалификация за обследване на сгради и ПС за ЕЕ.</p>
                </div>
                
            <div class="div7"> 
                <img src="/people/Metody_Nikiforov.jpg" alt="">
                <h2>Инж. Методи Никифоров</h2>
                <h4>Член на УС</h4>
                <p>
                Експерт в областта на енергийната ефективност към "Хас Строй" ЕООД, гр.Шумен- доказал компетентността и уменията си досега в обследване на обекти за енергийна ефективност.
                </p>
            </div>
            
            </div>
        </span>
    </main>
    </section>
    <style>
        main{
            display: flex;
            justify-content: space-evenly;
            gap: 2rem;
            flex-wrap: wrap;
            margin-top: 4em;
        }
        .div1{
            background-color: #3E8989;
            border-radius: .5em;
            width: 255px;
            padding-bottom: 1em;
            height: max-content;
        }
        span{
            width: 100vw;
            display: flex;
            justify-content: center;
        }

        .div1 img, .parent img{
            border-radius: .5em .5em .2em .2em;
    width: 100%;
        }
        .div1 h2, .parent h2{
            text-align: center;

        }
        .div1 p, .parent p{
            padding: 0 1em;
        }
        .div1 h4, .parent h4{
            text-align: center;
        font-weight: 400;
        }
        .parent div{
            background-color: #3E8989;
            border-radius: .5em;
        }
        .parent {
            width: 50em;
display: grid;
grid-template-columns: repeat(3, 1fr); /* 3 columns with equal width */
  grid-template-rows: repeat(2, 1fr);
gap: 1.1em;

}




    @media screen and (max-width: 924px) {
            .parent {
                grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)) !important; 
                width: 80%;
            }}

            @media screen and (max-width: 632px) {
                .div1{
                    min-width: 80%;

                }
            }

    </style>
    