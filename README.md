Описание результатов
================
Alexey Klimov
30 мая, 2017

-   Графики
-   [Линейное моделирование](#-)
    -   [Сравнимаем полученные модели](#--)
-   [Регрессия с регуляризацией](#--)
-   График
-   [Коэффициенты модели (только те, которые не равны нулю)](#-------)

Исходный код доступен в файле по ссылке: [README.Rmd](README.Rmd), скачать его можно с [репозитория на гитхабе](https://github.com/rhangelxs/r_socio_hse).

Графики
-------

<!--html_preserve-->

<script type="application/json" data-for="58924b257fc9">{"x":{"visdat":{"589214a429":["function () ","plotlyVisDat"]},"cur_data":"589214a429","attrs":{"589214a429":{"x":{},"y":{},"color":{},"alpha":1,"sizes":[10,100],"type":"box"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"xaxis":{"domain":[0,1],"title":"sex","type":"category","categoryorder":"array","categoryarray":["Men","Women"]},"yaxis":{"domain":[0,1],"title":"roc"},"hovermode":"closest","showlegend":true},"source":"A","config":{"modeBarButtonsToAdd":[{"name":"Collaborate","icon":{"width":1000,"ascent":500,"descent":-50,"path":"M487 375c7-10 9-23 5-36l-79-259c-3-12-11-23-22-31-11-8-22-12-35-12l-263 0c-15 0-29 5-43 15-13 10-23 23-28 37-5 13-5 25-1 37 0 0 0 3 1 7 1 5 1 8 1 11 0 2 0 4-1 6 0 3-1 5-1 6 1 2 2 4 3 6 1 2 2 4 4 6 2 3 4 5 5 7 5 7 9 16 13 26 4 10 7 19 9 26 0 2 0 5 0 9-1 4-1 6 0 8 0 2 2 5 4 8 3 3 5 5 5 7 4 6 8 15 12 26 4 11 7 19 7 26 1 1 0 4 0 9-1 4-1 7 0 8 1 2 3 5 6 8 4 4 6 6 6 7 4 5 8 13 13 24 4 11 7 20 7 28 1 1 0 4 0 7-1 3-1 6-1 7 0 2 1 4 3 6 1 1 3 4 5 6 2 3 3 5 5 6 1 2 3 5 4 9 2 3 3 7 5 10 1 3 2 6 4 10 2 4 4 7 6 9 2 3 4 5 7 7 3 2 7 3 11 3 3 0 8 0 13-1l0-1c7 2 12 2 14 2l218 0c14 0 25-5 32-16 8-10 10-23 6-37l-79-259c-7-22-13-37-20-43-7-7-19-10-37-10l-248 0c-5 0-9-2-11-5-2-3-2-7 0-12 4-13 18-20 41-20l264 0c5 0 10 2 16 5 5 3 8 6 10 11l85 282c2 5 2 10 2 17 7-3 13-7 17-13z m-304 0c-1-3-1-5 0-7 1-1 3-2 6-2l174 0c2 0 4 1 7 2 2 2 4 4 5 7l6 18c0 3 0 5-1 7-1 1-3 2-6 2l-173 0c-3 0-5-1-8-2-2-2-4-4-4-7z m-24-73c-1-3-1-5 0-7 2-2 3-2 6-2l174 0c2 0 5 0 7 2 3 2 4 4 5 7l6 18c1 2 0 5-1 6-1 2-3 3-5 3l-174 0c-3 0-5-1-7-3-3-1-4-4-5-6z"},"click":"function(gd) { \n        // is this being viewed in RStudio?\n        if (location.search == '?viewer_pane=1') {\n          alert('To learn about plotly for collaboration, visit:\\n https://cpsievert.github.io/plotly_book/plot-ly-for-collaboration.html');\n        } else {\n          window.open('https://cpsievert.github.io/plotly_book/plot-ly-for-collaboration.html', '_blank');\n        }\n      }"}],"cloud":false},"data":[{"x":["Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men","Men"],"y":[118,123,104,116,111,116,116,111,74,93,114,110,101,118,84,110,114,108,133,157,165,131,148,128,103,135,133,115,124,119,135,151,153,112,157,137,146,118,105,106,99,169,126,160,147,169,131,141,98,133,104,137,127,150,152,110,134,127,129,121,141,156,126,146,141,160,101,137,127,145,135,159,108,134,126,155,120,132,114,126,109,163,126,112,120,160,141,154,110,117,120,126,128,148,153,131,110,126,91,130,114,144,122,140,154,146,163,162,158,148,116,108,138,126,151,149,159,118,155,152,121,106,154,138,108,148,149,130,106,132,123,164,159,162,137,116,128,112,144,149,150,148,150,164,131,146,137,109],"type":"box","name":"Men","line":{"fillcolor":"rgba(102,194,165,0.5)","color":"rgba(102,194,165,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["Women","Women","Women","Women","Women","Women","Women","Women","Women","Women","Women","Women","Women","Women","Women","Women","Women"],"y":[109,88,132,114,79,114,111,132,115,94,89,76,120,151,137,144,146],"type":"box","name":"Women","line":{"fillcolor":"rgba(141,160,203,0.5)","color":"rgba(141,160,203,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1}},"base_url":"https://plot.ly"},"evals":["config.modeBarButtonsToAdd.0.click"],"jsHooks":{"render":[{"code":"function(el, x) { var ctConfig = crosstalk.var('plotlyCrosstalkOpts').set({\"on\":\"plotly_click\",\"persistent\":false,\"dynamic\":false,\"selectize\":false,\"opacityDim\":0.2,\"selected\":{\"opacity\":1}}); }","data":null}]}}</script>
<!--/html_preserve-->
![](README_files/figure-markdown_github/unnamed-chunk-5-1.png)

Линейное моделирование
----------------------

Сначала построим две модели:

1.  Модель для двух предикторов (lm0)
2.  Модель для двух предикторов с интеракцией между ними (lm1)

Показатели последней модели (lm1) с интеракцией:


    Call:
    lm(formula = roc ~ Oidep * Oiorg, data = data)

    Residuals:
       Min     1Q Median     3Q    Max 
    -51.73 -15.57   1.28  15.31  41.26 

    Coefficients:
                Estimate Std. Error t value Pr(>|t|)  
    (Intercept) 121.4591    47.6636    2.55    0.012 *
    Oidep        -1.9775     2.8275   -0.70    0.485  
    Oiorg         1.7235     2.5140    0.69    0.494  
    Oidep:Oiorg   0.0248     0.1428    0.17    0.863  
    ---
    Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    Residual standard error: 20 on 161 degrees of freedom
    Multiple R-squared:  0.122, Adjusted R-squared:  0.106 
    F-statistic: 7.45 on 3 and 161 DF,  p-value: 0.000106

Из вывода линейной модели нужно привести: **R*<sup>2</sup>, *N*, *p* − *v**a**l**u**e*, F-статистику*

Для каждого регрессора (предиктора): Как минимум *β* − *к**о**э**ф**ф**и**ц**и**е**н**т**а* и значимость + крайне желательно *t*-значние, либо *S**E*

### Сравнимаем полученные модели

Сравним наши модели с помощью метода (stepwise regression[1]) модель с интеракцией и модель без интеракции.

Для этого нам поможет пакет `lmSupport`, но в целом можно ориентироваться на AIC и BIC. Но в нашем случае достаточно воспользоваться ANOVA (или diff-test).

    SSE (Compact) =  62585 
    SSE (Augmented) =  62573 
    Delta R-Squared =  0.00016 
    Partial Eta-Squared (PRE) =  0.00019 
    F(1,161) = 0.03, p = 0.86

В результате добавление инетеракции (аддитивный эффект) улучшает предсказательные способности модели (*Δ**R*<sup>2</sup>) на 0.016%. Добавление интеракции значимо не улучшает показатели соответсвия модели данным (*p* = 0.86)

Нагляднее всего график:

![](README_files/figure-markdown_github/unnamed-chunk-10-1.png)

Регрессия с регуляризацией
--------------------------

В некоторых случаях в ручную отбирать регрессоры неудобно. Для этого можно использовать PLS (аля SEM), Ridge или Lasso.

Полезным будет техника разбиения выборки на обучающую и тестовую (80/20) из Machine Learning.

Для простоты предположим, что у нас нет никаких априорных представлений о модели. Попробуем найти самую удачную модель из всего датасета (включая исключительно числовые или факторные переменные).

В качестве интересующей нас (выходной) перменной мы зададим:

    [1] "roc"

Основаня проблема пакета `glmnet` в том, что ему на вход нужно подавать разреженные матрицы. Напишим для этого небольшую вспомогательную функцию (может даже не одну).

    Warning: attributes are not identical across measure variables; they will
    be dropped

В качестве предикторов числовых и категориальных предикторов у нас было 19 предиктор(а/ов): *comp*, *sex*, *age*, *tenure*, *promo*, *satis*, *position*, *norms1*, *norms2*, *Oidep*, *Oiorg*, *StK*, *StI*, *StRA*, *StRE*, *Pemo*, *Ptime*, *Femo* and *Ftime*.

1.  Сразу следует удалить предикторы, предсказательная сила которых слишком высокая (например, в этот список могут попасть компоненты выходной переменной). Мы же не хотим проверять очевидные вещи :)

2.  Затем следует вручную удалить предикторы, которые попали по ошибке (например, в этот список могут попасть компоненты выходной переменной). Внимательно посмотрим на вывод этой команды:

<table style="width:25%;">
<colgroup>
<col width="18%" />
<col width="6%" />
</colgroup>
<thead>
<tr class="header">
<th align="center">variable.y</th>
<th align="center">cor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">Femo</td>
<td align="center">0.42</td>
</tr>
<tr class="even">
<td align="center">StRE</td>
<td align="center">0.33</td>
</tr>
<tr class="odd">
<td align="center">Ftime</td>
<td align="center">0.32</td>
</tr>
<tr class="even">
<td align="center">norms1</td>
<td align="center">0.31</td>
</tr>
<tr class="odd">
<td align="center">norms2</td>
<td align="center">0.30</td>
</tr>
</tbody>
</table>

1.  Чтобы не столкнуться с проблемами мулитиколлинеарности или некорректного кодирования переменных, посмотрим на все предикторы, коэффциент корреляций которых между собой больше 0.9:

-   **variable.x**:

<!-- end of list -->
.

В *итоговый список* предикторов для LASSO регрессии у нас попали 19 переменных: *comp*, *sex*, *age*, *tenure*, *promo*, *satis*, *position*, *norms1*, *norms2*, *Oidep*, *Oiorg*, *StK*, *StI*, *StRA*, *StRE*, *Pemo*, *Ptime*, *Femo* and *Ftime*

По умолчанию `glmnet` строит LASSO модель (`alpha` = 1), если нужна Ridged регрессию, то нужно указать параметр `alpha` = 0.

Выбираем лучшую лямбду

<table style="width:36%;">
<colgroup>
<col width="18%" />
<col width="18%" />
</colgroup>
<thead>
<tr class="header">
<th align="center">lambda.min</th>
<th align="center">lambda.1se</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">1.292</td>
<td align="center">3.276</td>
</tr>
</tbody>
</table>

    [1] 3.3

График
------

![](README_files/figure-markdown_github/unnamed-chunk-23-1.png)

Коэффициенты модели (только те, которые не равны нулю)
------------------------------------------------------

<table style="width:69%;">
<colgroup>
<col width="16%" />
<col width="9%" />
<col width="15%" />
<col width="12%" />
<col width="15%" />
</colgroup>
<thead>
<tr class="header">
<th align="center">term</th>
<th align="center">step</th>
<th align="center">estimate</th>
<th align="center">lambda</th>
<th align="center">dev.ratio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">(Intercept)</td>
<td align="center">1</td>
<td align="center">115.5</td>
<td align="center">3.276</td>
<td align="center">0.2342</td>
</tr>
<tr class="even">
<td align="center">satis</td>
<td align="center">1</td>
<td align="center">0.3289</td>
<td align="center">3.276</td>
<td align="center">0.2342</td>
</tr>
<tr class="odd">
<td align="center">norms2</td>
<td align="center">1</td>
<td align="center">2.449</td>
<td align="center">3.276</td>
<td align="center">0.2342</td>
</tr>
<tr class="even">
<td align="center">Oiorg</td>
<td align="center">1</td>
<td align="center">0.1468</td>
<td align="center">3.276</td>
<td align="center">0.2342</td>
</tr>
<tr class="odd">
<td align="center">StRA</td>
<td align="center">1</td>
<td align="center">-0.1222</td>
<td align="center">3.276</td>
<td align="center">0.2342</td>
</tr>
<tr class="even">
<td align="center">StRE</td>
<td align="center">1</td>
<td align="center">0.06668</td>
<td align="center">3.276</td>
<td align="center">0.2342</td>
</tr>
<tr class="odd">
<td align="center">Femo</td>
<td align="center">1</td>
<td align="center">1.753</td>
<td align="center">3.276</td>
<td align="center">0.2342</td>
</tr>
</tbody>
</table>

[1] почему этот старый и добрый метод не современный написано тут: <https://stats.stackexchange.com/questions/13686/what-are-modern-easily-used-alternatives-to-stepwise-regression>
