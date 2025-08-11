# Part 46: Integrated generic resource: Visual presentation

Этот документ определяет интегрированные общие ресурсы для описания визуального представления.

Визуальное представление объединяется с данными об изделии и передается между системами с целью, чтобы принимающая система могла создать одно или несколько изображений изделия (и связанной информации), подходящих для восприятия человеком. 

Схема содержит сущности для описания желаемого внешнего вида информации об изделии на изображении. Создание фактического изображения на основе полученных данных (информации об изделии и о визуальном представлении) остается за принимающей системой.  Фактическое изображение может отличаться от желаемого внешнего вида из-за ограничений в возможностях графических систем. 

Информация о продукте может быть визуализирована двумя способами: 

1) с помощью реалистичных изображений в натуральную величину в соответствии с правилами проективной геометрии, распространения и отражения света, 
2) с помощью символических изображений, соответствующих правилам выполнения чертежей и применяемым условным обозначениям. 

Этот документ поддерживает оба типа визуализации. 

Эти два типа визуализации требуют различных графических преобразований, которые могут быть объединены в одном изображении. 

В рамках данного документа описано следующее:
- связь между данными об изделии, определенными в других частях стандарта ISO 10303, и данными визуализации; 
- поддержка графических функций в соответствии с действующими графическими стандартами ISO;
- определение атрибутов стиля визуализации для реалистичной и символической визуализации геометрических и негеометрических отображаемых элементов, содержащихся в данных изделия; 
- управление допусками аппроксимации для элементов геометрического представления; 
- методы определения внешнего вида символов в шрифтах; 
- поддержка внешних символьных шрифтов и обозначений; 
- управление изображениями с помощью механизма слоев; 
- вложенность областей представления; 
- внешняя связь изображений с триангулированной (фасетной) геометрией; 
- связь информации о цвете с вершинами триангулированной (фасетной) геометрии. 

Нижеследующее выходит за рамки данного документа: 
- определение информации об изделии; 
- обмен чисто графической информацией без какой-либо связи с информацией об изделии; 
- определение содержимого символьных шрифтов и библиотек символов.

=========================================================================

This document specifies the integrated generic resource constructs for visual presentation. Presentation data as provided in this document are combined with product data and are exchanged together between systems with the aim that the receiving system can construct one or several pictures of the product information suitable for human perception.
This document specifies the generic resources required to describe the desired visual appearance of product information in its picture. The actual generation of the picture from the product information and its presentation data is left to the receiving system. The actual depiction can deviate from this target because of limitations in the capabilities of graphics systems.

Product information can be visualized in two ways, either by realistic, life-like images according to the rules of projective geometry and light propagation and reflection, or by symbolic presentations that conform with draughting standards and conventions. This document supports both types of presentations. The two types of visualization processes require different kinds of graphical transformations and these can be combined in the same picture.

The following are within the scope of this document:
- association between product data defined by other parts of ISO 10303 and presentation data;
- support of graphics functionality in compliance with current ISO graphics standards;
- definition of presentation style attributes for realistic and symbolic visualizations of geometric and non-geometric displayable elements in the product information;
- control of approximation tolerances for geometric presentation elements;
- methods for defining the appearance of characters and symbols in fonts;
- support of externally defined character fonts and symbols;
- image control by a layer mechanism;
- nesting of presentation areas;
 -external image association to tessellated geometry;
- association of colour information with vertices of tessellated geometry.

The following are outside the scope of this document:

- definition of product information;
- exchange of purely graphical information without any relationship to product information;
- definition of the contents of character font and symbol libraries.
