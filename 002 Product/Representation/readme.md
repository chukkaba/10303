## Схема представления

Representation_schema определяет общую структуру представления (representation). 

Для представления некоторого аспекта данных об изделии (например, свойства изделия) могут быть созданы **коллекции данных**. Каждый элемент в такой коллекции является элементом представления (representation_item). Примером свойства, которое может быть представлено, является форма изделия. 

В этой части стандарта ISO 10303 не указано, какой аспект или свойство должно быть представлено. Просто определяется понятие **"представление"** для использования в других частях стандарта ISO 10303.

Когда элементы представления (representation_item) собираются в определенную коллекцию данных для создания представления (representation), они используют общий контекст, который связан с представлением. Этот контекст называется контекстом представления (representation_context).

Не все элементы данных об изделии входят в представление. Те элементы, которые могут входить в представление, определяются как элементы представления (representation_item). Элементы представления - это те элементы, которые имеют значение только в рамках определенного контекста. Например, точка - это элемент представления, который имеет значение только в рамках контекста (координатного пространства). В отличие от этого, имя человека не является элементом представления, поскольку оно имеет значение отдельно от любого контекста.

Элемент представления может входить в представление (как сказано выше), а также может поддерживать определение других элементов представления. Данная часть стандарта ISO 10303 допускает это различие.

Коллекция данных об изделии может содержать множество элементов представления, каждый из которых участвует в одном или нескольких представлениях. Эти представления могут быть связаны между собой, образуя структуру, которая также связывает контексты представления. Затем эта структура может быть использована для определения того, какие элементы представления могут быть связаны друг с другом значимым образом. Например, расстояние между точками имеет смысл только в том случае, если системы координат, в которых эти точки определены, могут быть связаны между собой.

Представления, не связанные в одном контексте, могут быть связаны в другом. Рассмотрим представление формы детали и ее компонентов. Форма каждого компонента может быть представлена как независимое понятие, не связанное с формой других компонентов. Однако в контексте собранной детали формы компонентов взаимосвязаны.

Аспект данных об изделии может иметь ноль, одно или множество представлений, ни одно из которых не является концепцией (изделия?) как таковой. Например, форма детали может быть представлена набором как двумерных геометрических данных, так и конструктивной твердотельной геометрией (constructive solid geometry). Любое представление является идеализацией формы.

Каждое представление не обязательно является полной моделью какого-либо аспекта данных об изделии, но оно может представлять модель аспекта, подходящую для конкретных применений. Ни одно из представлений формы из предыдущего абзаца не  является обязательно полным представлением концепции формы (???). Еще одно представление формы может включать информацию о допусках. Скорее всего, каждое представление подходит для какого-то конкретного применения или подхода.

==================================================================


The representation_schema specifies the overall structure for representation. Collections of elements can be formed to act as the representation of some aspect of product data, such as a property of a product. Each element in such a collection is a representation item. An example of a property that can be represented is the shape of a product. The aspect or property that is being represented is not specified in this part of ISO 10303. Instead the subject of the representation is defined where the capabilities for representation are used in other parts of ISO 10303.

When representation items are collected to participate in a representation, they share a common context which is associated with the representation. This context is referred to as a representation context.

Not all elements of product data participate in representations. Those items which can participate in representations are defined to be representation items. Representation items are those elements that have complete meaning only when associated with a context. As an example, a point is a representation item which is only meaningful within a context (a coordinate space). In contrast, the name of a person is not a representation item because it has meaning separate from any context.

In addition to being an element of representation, a representation item can also support the definition of other representation items. This part of ISO 10303 allows for this distinction.

A collection of product data can contain numerous representation items, each participating in one or more representations. These representations can be related to form a structure which also relates the representation contexts. This structure can then be used to determine which representation items can be related to each other in a meaningful way. As an example, distance between points is only meaningful if the coordinate systems in which the points are defined can be related.

Representations that are unrelated in one context can be related in another. Consider the representation of the shape of a part and its components. The shape of each component can be represented as an independent concept, unrelated to the shape of the other components. In the context of the assembled part, however, the shapes of the components are related.

An aspect of product data can have zero, one, or multiple representations, none of which are the concept itself. For example, the shape of a part can be represented by a collection both of two-dimensional geometry and of constructive solid geometry. Either representation is an idealization of the shape.

Each representation is not necessarily a complete model of some aspect of product data, but it can represent a model of the aspect that is suitable for specific applications. Neither shape representation in the previous paragraph is necessarily a complete representation of the shape concept. Another shape representation might include tolerance information. Rather, each representation is suitable to some specific application’s view or approach.