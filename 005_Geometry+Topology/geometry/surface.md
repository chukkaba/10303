# Описание поверхности
![](source/surface.png)

Кривая - это непрерывное отображение связного множества в двумерном пространстве параметров (u,v) в точки трехмерного пространства. Отображаемое множество называется областью определения поверхности. Значение радиус-вектора и частных производных поверхности, вычисленных за пределами области определения в общем случае не определено.

Перечень классов
- elementary_surface
- plane
- cylindrical_surface
- cylindrical_surface
- cylindrical_surface
- toroidal_surface
- degenerate_toroidal_surface
- ration_b_spline_surface
- curve_bounded_surface
- offset_surface
- surface_replica

## Класс elementary_surface

Базовый класс для определения элементарных поврехностей. Содержит локальную систему координат, в которой задается элементарная поверхность.

\vec{c} - радиус-вектор начала системы координат.
\vec{OX}, \vec{OY}, \vec{OZ} - базисные векторы системы координат.

## Класс plane

Плоскость. Область определения бесконечная по u и по v. 

Радиус-вектор вычисляется по формуле:

\vec{r}(u,v) = \vec{C} + \vec{OX} \cdot u + \vec{OY} \cdot v .

## Класс cylindrical_surface

Цилиндрическая поверхность. Определяется значением радиуса R - числом с плавающей точкой больше нуля (ИЛИ МЕТРИЧЕСКОЙ ПОГРЕШНОСТИ).

Область определения по u (0, 2 \cdot \pi) и бесконечная по v.

Радиус-вектор вычисляется по формуле:

\vec{r}(u,v) = \vec{C} + \vec{OX} \cdot R \cdot \cos(u) + \vec{OY} \cdot R \cdot \sin(u) + \vec{OZ} \cdot v .

## Класс cylindrical_surface

Коническая поверхность. Определяется значением радиуса R - числом с плавающей точкой больше нуля (ИЛИ МЕТРИЧЕСКОЙ ПОГРЕШНОСТИ) и угла раскрытия \theta.

Область определения по u от (0, 2 \cdot \pi) и бесконечная по v.

Радиус-вектор вычисляется по формуле:

\vec{r}(u,v) = \vec{C} + \vec{OX} \cdot (R + \tg(\theta) \cdot v) \cdot \cos(u) + \vec{OY} \cdot (R + \tg(\theta) \cdot v) \cdot \sin(u) + \vec{OZ} \cdot v .


## Класс cylindrical_surface

Сферическая поверхность. Определяется значением радиуса R - числом с плавающей точкой больше нуля (ИЛИ МЕТРИЧЕСКОЙ ПОГРЕШНОСТИ) и угла раскрытия \theta.

Область определения по u от (0, 2 \cdot \pi) и по v (-\pi \cdot 0.5, \pi \cdot 0.5).

Радиус-вектор вычисляется по формуле:

\vec{r}(u,v) = \vec{C} + \vec{OX} \cdot R \cdot \cos(u) \cdot \sin(v) + \vec{OY} \cdot R \cdot \sin(u) \cdot \sin(v) + \vec{OZ} \cdot R \cdot \cos(v)

## Класс toroidal_surface

Тороидальная поврехность. Определяется значением радиусов R_major и R_minor.

Область определения по u от (0, 2 \cdot \pi) и по v (0, \pi \cdot 2).

Радиус-вектор вычисляется по формуле:

\vec{r}(u,v) = \vec{C} + \vec{OX} \cdot (R_{major} + R_{minor}\cos(v)\cos (u) )+ \vec{OY} \cdot (R_{major} + R_{minor} \cdot \cos(v) \sin(u)) + \vec{OZ} \cdot R_{minor} \cdot \sin( v )

## Класс toroidegenerate_toroidal_surfacedal_surface

Вырожденная тороидальная поврехность. Наследует поля R_major и R_minor от класса toroidal_surface. Дополнительно определяется булевым флагом select_outer, который отвечает за форму: яблоко в случае ИСТИНА, лимон в случае ЛОЖЬ.

Область определения по u от (0, 2 \cdot \pi).

Для тора-яблока область определения по v (\arctan(\frac{R_{minor}}{R_{major}}) - \pi,\pi -  \arctan(\frac{R_{minor}}{R_{major}})).

Для тора-лимона область определения по v ( - \arctan(\frac{R_{minor}}{R_{major}}),\arctan(\frac{R_{minor}}{R_{major}})).

Радиус-вектор тора-яблока вычисляется по формуле:

\vec{r}(u,v) = \vec{C} + \vec{OX} \cdot (R_{major} + R_{minor}\cos(v)\cos (u) )+ \vec{OY} \cdot (R_{major} + R_{minor} \cdot \cos(v) \sin(u)) + \vec{OZ} \cdot R_{minor} \cdot \sin( v ).

Радиус-вектор тора-лимона вычисляется по формуле:

\vec{r}(u,v) = \vec{C} + \vec{OX} \cdot (-R_{major} + R_{minor}\cos(v)\cos (u) )+ \vec{OY} \cdot (-R_{major} + R_{minor} \cdot \cos(v) \sin(u)) + \vec{OZ} \cdot R_{minor} \cdot \sin( v ).

## Класс offset_surface

Эквидистантная поверхность. Определяется опорной поверхностью и величиной смещения.

Область определения такая же, какая у опорной поврехности.

Радиус-вектор вычисляется по формуле:

\vec{r}(u,v) = \vec{r_{basis}}(u,v) + \vec{n}(u, v) \cdot offset,

где r_{bais} - радиус-вектор опорной поверхности,
n - нормированный вектор нормал опорной поверхности,
offset - величина смещения.