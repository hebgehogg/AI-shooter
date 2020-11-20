# AIShooter
Упрощённый вариант Survival Game на Unreal Engine 4
- Овчинникова Алина 
- hebgehogg@gmail.com
- тел: +7(950) 446-12-02

### Версия 4.25.3


# Design doc

### Concept: 

Platforms: Windows.  
Technologies: Unreal Engine 4.  
Languages:  английский.  
Genre: Survival Game.  
Emotions: снятие стресса после работы/учебы (убийство времени).  
Rating:  7+ (E — Everyone).  
User Number:  single-player.  
Gameplay time:  1 минута +- 5 секунд.  
Maine mechanic:  добраться из точки "А" в "В".  
Setting:  убийство ИИ, движение вперед.  
Goal: добраться до точки "В" живым.  


### Setting: 

Визуальная часть игры имитирует туннель, в котором игрока ждет куча препятствий и враги (ИИ).  
Сеттинг мрачный, он разбавлен неоновыми элементами - это и есть фишка дизайна, это придает особое настроение.  
Процедурная генерация мира создается при помощи уникально сбалансированного алгоритма, который создан эмпирическим путем.
Основная цель пройти мимо ИИ, которые будут пытаться тебя убить fairball`ами, и добраться до точки "В" живым. 


### Game Character: 

Персонаж - стандартнвая фигурка из UE4.  
Камера установлена от 1 лица.  
Персонаж имеет взаимодейсивия с объектами на карте - врагами, fairball`ами, препядствиями и самой картой.  
Описание управления и уровней будет ниже.  


# Управление

* WASD - передвижение
* ЛКМ - выстрел
* R - рестарт игры

### Interface: 

> Стартовая локация  

![Окно](https://github.com/hebgehogg/AIShooter/blob/main/Photos/Start.png)

> Конечная локация  

![Окно](https://github.com/hebgehogg/AIShooter/blob/main/Photos/PointB.png)

> Окно окончания игры - успешное  

![Окно](https://github.com/hebgehogg/AIShooter/blob/main/Photos/GameEnd.png)

> Окно выходящее при смерти персонажа (конце игры)  

![Окно](https://github.com/hebgehogg/AIShooter/blob/main/Photos/Death.png)

> Изменеие жизни при ударе 1/3 (на фото при выходе из зоны поражения немного возсановилось)  
Востановление 0.2% в секнунду только вне зоны поражения.  
Отображение настроено через прогресбар.

![Окно](https://github.com/hebgehogg/AIShooter/blob/main/Photos/Damage.png)

> Регенерация

![Окно](https://github.com/hebgehogg/AIShooter/blob/main/Photos/Regen.png)


# ИИ враг

Врвг бежит на ирока, из него вылетают fairball`ы.

> Вага бегущий на персонажа

![Враг](https://github.com/hebgehogg/AIShooter/blob/main/Photos/AI.png)


# Firballs 

Ими стреляет как и игрок, так и ИИ в него.

![Шар](https://github.com/hebgehogg/AIShooter/blob/main/Photos/FairBall.png)


# Level design: 

Уровень в игре 1, он длиться примерно 1 минуту, в завсисимости от навыков игрока, карта предствляет из себя 1 длинный блок с препядствиями, разделенными на секции.


# Блоки

> Блок регенерации - это Actor, наложенный на весь пол, который не виден пользователю, но он не перекрывает блоки, где ИИ может видеть/атаковать персонажа.

> Блок активации ИИ - при заходе на этот блок ИИ начинает стрелять fairball`ами и преследовать игрока.

![Блок](https://github.com/hebgehogg/AIShooter/blob/main/Photos/PinkBlock.png)


# Оформление дизайна

Все блоки, заставки и картинки были нарисованы и смоделированы мной.  
Кроме картинкки для анимации Firballs: https://www.mediafire.com/file/e4ccbd9sbgnvwcz/FireballFiles.zip/file





