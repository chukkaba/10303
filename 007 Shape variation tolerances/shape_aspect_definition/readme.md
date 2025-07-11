## Shape aspect definition schema

### 0 Термины (как по русски назвать используемые понятия):

**shape_aspect** - 

**derived_shape_aspect** - 

**datum_system** - 

**datum_reference_compartments** - 

### 1 Общие положения

Целью схемы shape_aspect_definition является определение пространственных характеристик формы, которые требуются для определения размеров и допусков. Эта схема описывает представления (representations) для derived_shape_aspect и datum_system. 

derived_shape_aspect - это shape_aspect, который разработан на основе определенной формы изделия, но не требуется для определения формы изделия. 

datum_system - это shape_aspect, который указывает базу, от которой задаются геометрические допуски (не уверена в переводе). 

derived_shape_aspect и datum_system - это аспекты формы, которые требуются для определения размеров и допусков к форме, размеру, ориентации и местоположению формы изделия.

### 2 Технические пояснения

Форма изделия (product shape) - это понятие формы как свойства, характеризующего изделие. 

Геометрические модели и технические чертежи - это формальные методы, используемые для представления формы изделия. 

Размеры и допуски (Dimensions and tolerances) - это элементы определения формы изделия, которые не зависят от того, как представлена форма. Размеры могут быть явно определены как часть характеристик формы, неявно включены в геометрическую модель, представляющую форму, или явно представлены на двумерном чертеже или на аннотированной 2D или 3D модели.

shape_aspect и все его подтипы, такие как derived_shape_aspect, являются элементами формы изделия, представленными product_definition_shape. Параметр product_definition_shape может представлять номинальную модель изделия или извлеченные поверхности заготовки, как указано в прикладных протоколах или прикладных модулях, использующих эти концепции. Для целей данного документа применяется следующее соответствие концепциям ISO 14660-1 и ISO/TS 17450-1:

- параметр shape_aspect для номинальной модели с определяющим атрибутом, установленным в значение TRUE, представляет собой номинальный интегральный признак;

- параметр derived_shape_aspect для номинальной модели представляет собой номинальный производный элемент;

- параметр shape_aspect для выделенной поверхности заготовки с определяющим атрибутом, равным TRUE, представляет либо выделенный интегральный элемент, либо связанный с ним интегральный элемент;

- параметр derived_shape_aspect для выделенной поверхности заготовки представляет собой либо выделенный производный элемент, либо связанный с ним производный элемент.

ПРИМЕЧАНИЕ 1. Реальная поверхность заготовки и ее реальные интегральные характеристики недоступны для компьютерной обработки.

Размеры могут быть указаны как для всей формы изделия, так и для отдельных элементов формы. Эта схема дополняет параметры формы и взаимосвязи между ними в качестве механизма определения размеров и допусков. Форма объекта, взаимосвязи между элементами формы объекта и их заданные размеры и допуски всегда определяются в контексте product_definition_shape. Эти размеры и допуски могут быть представлены в виде элементов геометрических моделей или технических чертежей.

datum_system представляет собой последние ячейки фрейма допусков (last compartments of a tolerance frame), которые ссылаются на данные и задают модификаторы. datum_system состоит из списка от одного до трех datum_reference_compartments. Элемент datum_reference_compartment либо ссылается непосредственно на элемент данных, либо ссылается на список элементов datum_reference_elements для установления общего элемента данных. Исходные данные либо определяются параметром datum_feature, либо устанавливаются одним или несколькими объектами datum_targets. Если не указано иное, должны применяться правила, регулирующие систему данных, исходное число, элемент данных и цель данных, определенные в стандарте ISO 5459.

ПРИМЕЧАНИЕ 2 В качестве альтернативы можно использовать базовую систему, базовую функцию и целевой объект в соответствии со спецификациями, приведенными в ASME Y14.5-2009 [11].

С целью определения размеров и допусков эта схема определяет концепцию derived_shape_aspect. derived_shape_aspect - это shape_aspect, который определяется на основе конкретного способа, которым он соотносится с другим аспектом формы. Параметр derived_shape_aspect используется в сочетании со связанными элементами shape_aspect для указания размеров и допусков. Конкретная геометрия, которая может представлять derived_shape_aspect и shape_aspect, которые обеспечивают связь определения, не входит в область действия этой схемы. Геометрия, структура представления и их связь с элементами размеров и допусков, указанными в этой части, определены в стандартах ISO 10303-41, ISO 10303-42 и ISO 10303-43. Здесь указано только общее понятие derived_shape_aspect. В протоколах приложений могут указываться другие элементы derived_shape_aspect в дополнение к предоставленным.

Различные типы механизмов сбора shape_aspects предоставляются composite_shape_aspect и его подтипами. Допуски на размеры и геометрические формы, применяемые к объекту composite_group_shape_aspect, применяются индивидуально ко всем его элементам. При применении размеров и геометрических допусков к continuous_shape_aspect, between_shape_aspect или all_around_shape_aspect они применяются только к коллекции в целом.