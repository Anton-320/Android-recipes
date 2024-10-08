# Требования к проекту

## Содержание

[1 Введение](#1)  
[1.1 Назначение](#11)  
[1.2 Бизнес-требования](#12)  
[1.2.1 Исходные данные](#121)  
[1.2.2 Возможности бизнеса](#122)  
[1.2.3 Границы проекта](#123)  
[1.3 Существующие аналоги](#13)  
[2 Требования пользователя](#2)  
[2.1 Программные интерфейсы](#21)  
[2.2 Интерфейс пользователя](#22)  
[2.3 Характеристики пользователей](#23)  
[2.3.1 Классы пользователей](#231)  
[2.3.2 Аудитория приложения](#232)  
[2.4 Предположения и зависимости](#24)  
[3 Системные требования](#3)  
[3.1 Функциональные требования](#31)  
[3.1.1 Авторизация](#311)  
[3.1.2 Просмотр рецептов блюд](#312)  
[3.1.3 Добавление рецептов](#313)  
[3.1.4 Удаление рецептов](#314)  
[3.1.5 Редактирование рецептов](#315)  
[3.2 Нефункциональные требования](#32)  

<a name="1"/>

## 1 Введение

<a name="11"/>

### 1.1 Назначение
В этом документе описаны функциональные и нефункциональные требования к приложению «Книга рецептов» для Android.

<a name="12"/>

### 1.2 Бизнес требования

<a name="121"/>

#### 1.2.1 Исходные данные

В настоящее время многие люди увлекаются готовкой. Некоторые рецепты они берут из интернета, некоторые — придумывают сами. Со временем количество понравившихся рецептов у таких людей растёт, а удерживать всех их в голове становится всё тяжелее. Поэтому часто у людей возникает желание сохранить где-нибудь понравившиеся им рецепты.

<a name="122"/>

#### 1.2.2 Возможности бизнеса
Долгое время люди записывали свои рецепты в обыкновенные бумажные тетради. Но в настоящее время, когда большинству людей удобнее пользоваться смартфоном, чем тетрадью и ручкой, всё больше возрастает потребность в приложении, в которое можно будет удобно сохранять и просматривать понравившиеся рецепты.

<a name="123"/>

#### 1.2.3 Границы проекта
Приложение "Книга рецептов" позволит пользователям удобно записывать свои любимые рецепты и сохранять их на мобильном устройстве. Также у пользователя будет возможность поиска записанных им рецептов. Приложение не будет поддерживать расчет калорийности и рекламу.

<a name="13">

### 1.3 Существующие аналоги
В настоящее существует немало мобильных приложений для сохранений рецептов. Неплохим примером будут "Recipe bookk App" и "Cookmate".

<a name="2"/>

## 2 Требования пользователя

<a name="21"/>

### 2.1 Программные интерфейсы
Приложение будет иметь собственную базу данных, расположенную локально на мобильном устройстве. С внешними API приложение взаимодействовать не будет.

<a name="22"/>

### 2.2 Интерфейс пользователя
Перед переходом на главную страницу со своими рецептами пользователь должен зарегистрироваться или войти в уже существующий аккаунт. Ниже представлены страница регистрации и страница входа в аккаунт. На странице авторизации пользователь должен будет ввести логин и пароль при входе на существующий аккаунт.

Страница регистрации

![Страница регистрации](https://github.com/Anton-320/Android-recipes/blob/main/docs/mockups/sign_up_page.png)

Страница входа в аккаунт

![Страница входа в аккаунт](https://github.com/Anton-320/Android-recipes/blob/main/docs/mockups/sign_in_page.png)

Главная страница приложения отображает список добавленных пользователями рецептов, также сверху есть строка поиска. Ниже представлена главная страница.

Главная страница

![Главная страница](https://github.com/Anton-320/Android-recipes/blob/main/docs/mockups/main_page.png)

При переходе на отдельную страницу рецепта пользователь увидит описание блюда, ингредиенты и инструкции по приготовлению. Ниже представлен пример страницы рецепта.

Страница рецепта

![Страница рецепта](https://github.com/Anton-320/Android-recipes/blob/main/docs/mockups/recipe_page.png)

С главной страницы пользователь может перейти на страницу добавления рецепта. По структуре она аналогична странице рецепта. Ниже представлена страница добавления рецепта. 

Страница добавления рецепта

![Страница добавления рецепта](https://github.com/Anton-320/Android-recipes/blob/main/docs/mockups/recipe_add_page.png)

Чтобы редактировать или удалить ингредиент пользователь должен будет зажать вкладку с ингредиентом и в выпавшем диалоговом окне выбрать редактировать или удалить соответственно.

Пользователь сможет редактировать или удалить рецепт, в главном меню зажав вкладку с рецептом и выбрав в диалоговом окне редактировать или удалить соответственно. Окно для регистрации будет аналогичным окну создания (добвления) рецепта.

<a name="23"/>

### 2.3 Характеристики пользователей

<a name="231">

#### 2.3.1 Классы пользователей
В описываемом приложении есть только один класс пользователя — авторизованный пользователь. 

<a name="232">

#### 2.3.2 Аудитория приложения
Данное приложение рассчитано на обычных пользователей, интересующихся кулинарией. Уровень образования не имеет значения. Для использования данного приложения пользователю необходим средний уровень технической грамотности, базовые навыки работы с мобильными приложениями.

<a name="24"/>

### 2.4 Предположения и зависимости
Приложение предполагает стабильное оработу мобильного устройства для работы с самим приложением и с базой данных рецептов.
Пользователи будут регистрироваться локально на одном мобильном устройстве.

<a name="3"/>

## 3 Системные требования

<a name="31"/>

### 3.1 Функциональные требования

<a name="311">

#### 3.1.1 Авторизация
При входе в приложение пользователь должен зарегистрироваться или зайти в свой аккаунт

| Функция | Требование |
|:---|:---|
| Регистрация нового пользователя | Приложение запрашивает имя и пароль. Пользователь вводит данные и регистрируется |
| Вход с авторизацией | Приложение запрашивает имя и пароль, после чего пользователь входит в профиль |

<a name="312">

#### 3.1.2 Просмотр рецептов блюд
На главной странице пользователь может просмотреть рецеты блюд а также осуществлять поиск по ним.

| Функция | Требования | 
|:---|:---|
| Просмотр всех добавленных рецептов | Все добавленные пользователем блюда отображаются при входе на главную страницу или при нажатии на кнопку "Все блюда" |
| Просмотр конкретного рецепта | После нажатия на рецепт в списке, открывается подробная информация о нём |

<a name="313">

#### 3.1.3 Добавление рецептов
У пользователя есть возможность добавлять новые рецепты.

| Функция | Требования | 
|:---|:---|
| Добавление нового рецепта | Приложение запрашивает название, время приготовления, количество порций, ингридиенты и инструкции по приготовлению, после чего рецепт появляется в списке рецептов |

<a name="314">

#### 3.1.4 Удаление рецептов
У пользователя есть возможность удалять свои рецепты.

| Функция | Требования | 
|:---|:---|
| Удаление рецепта | Пользователь имеет возможность удалить существующий рецепт |

<a name="315">

#### 3.1.5 Редактирование рецептов
Пользователь может редактировать свой рецепт.

| Функция | Требования | 
|:---|:---|
| Редактирование рецепта | Пользователь имеет возможность редактировать существующий рецепт. Всё, что запрашивало приложение при создании рецепта, может быть изменено |

<a name="32"/>

### 3.2	Нефункциональные требования

1. Надежность: Приложение должно корректно работать при корректной работе базы данных на устройстве и корректной работе самого устройства. Отказы при выполнении операций (например, авторизация, загрузка рецептов) должны быть сведены к минимуму.
2. Безопасность: Важно обеспечить защиту данных пользователей (рецепты, личные предпочтения) через безопасную авторизацию.
3. Производительность: Приложение должно быстро загружать рецепты, независимо от объема данных и 
оптимально использовать ресурсы устройства.
