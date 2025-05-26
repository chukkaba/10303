Нахначение схемы material_property_definition_schema  - это ассоциация изделия со свойствами, описаниями состава изделия и идентификацией материала.

Основные понятия и допущения:

- свойства материала являются репрезентативными для всех технических свойств, которые определяются с помощью определенного метода тестирования;
- технические свойства характеризуют некоторые аспекты поведения изделия;
- состав изделия описывается спецификацией типа, количества и расположения его компонентов.

Технические характеристики могут быть определены на основе измерений на изделии в целом, на образце, взятом из изделия каким-либо способом, например, путем резки, или на совершенно отдельном образце для испытаний, полученном путем обработки таким же образом, как и само изделие. Применение результатов, полученных на испытательном образце, ко всему изделию зависит от отношения образца к изделию, поскольку в результате производственного процесса изделие может быть неоднородным или изотропным.

На значения большинства свойств пизделия влияет производственный процесс. Производственный процесс может влиять на тип и количество элементов, из которых состоит изделие, а также на их форму и расположение. Этими элементами могут быть атомы, молекулы или другие их агрегаты в виде отдельных форм, таких как кристаллы, волокна или объемы полукристаллических или стеклообразных материалов. Расположение элементов определяет структуру материала изделия.

Структура материала твердого изделия может быть как однородной, так и неоднородной, или представлять собой смесь твердых веществ, например, в композитных конструкциях. Полное описание конструкции включает в себя соотношение любых предпочтительно выровненных элементов конструкции друг с другом и с изделием.

Значения технических характеристик также могут быть присвоены продукту путем ссылки на спецификацию, из расчета или предположения.

**ПРИМЕР 1** Производитель может изготовить продукт в соответствии со спецификацией и вместо того, чтобы сообщать о фактических измерениях в конкретной партии продукта, он может сообщить номинальное значение, указанное в спецификации.

**ПРИМЕР 2** Химик может выполнить расчеты, используя предполагаемые значения прочности соединения, чтобы предсказать прочность полимера, который никогда не синтезировался.

**ПРИМЕР 3** Инженер, проводящий конечно-элементный анализ детали, может присвоить значения свойств, чтобы предсказать потенциальные характеристики продукта в зависимости от свойств.

=====================================================================

The subjects of the material_property_representation_schema are the associations of a product with: a property, descriptions of product composition and of material identification.

The following are the fundamental concepts and assumptions relating to the material_property_representation_schema:

- material properties are representative of all engineering properties that are defined by a specified testing method;
- an engineering property characterizes some aspect of the behaviour of a product;
- the composition of a product is described by the specification of the type, amounts and arrangement of its constituents.

The engineering properties may be determined from measurements on the product as a whole, on a sample taken from the product in some way such as cutting, or an entirely separate test piece prepared by processing in the same way as the product. The application of the results derived from a test piece to the whole product is dependent on the relationship to the sample to the product because, as a result of the manufacturing process, the product may not be either homogeneous or isotropic.

The values of most properties of a product are influenced by the effect that the manufacturing process has had on the product. The manufacturing process may affect the type and amounts of the units that make up the product and their form and arrangement. These units may be atoms, molecules or other aggregates of these into discrete forms such as crystals, fibres or volumes of semi-crystalline or glassy solids. The arrangement of the units is the material structure of the product.

The material structure of a solid product may be either homogeneous or heterogeneous, or a mixture of solids such as in composite structure. A complete specification of the structure includes the relationship of any preferentially aligned elements of the structure to each other and to the product.

Values for an engineering property may also be assigned to a product by reference to a specification, by calculation, or by assumption.

EXAMPLE 1   A manufacturer may make a product to a specification and, instead of reporting actual measurements from a specific batch of the product, he may report the nominal value indicated in the specification.

EXAMPLE 2   A chemist may perform calculations using assumed values of bond strengths to predict the strength of a polymer that has never been synthesised.

EXAMPLE 3   An engineer performing a finite element analysis on part might assign property values to predict potential product performance as a function of the property.