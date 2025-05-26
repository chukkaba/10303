Назначение схемы material_property_representation_schema -  представление технических свойств и условий, при которых эти представления свойств действительны.

Основные понятия и допущения:

- возможно множественное представление объекта, включая использование числовых значений, параметрических или фундаментальных уравнений, графических представлений и нечисловых значений;
ПРИМЕЧАНИЕ. Различие между понятием и представлением понятия описано в стандарте ISO 10303-43

- значение свойства может быть присвоено или измерено;
- если значение измеряется, то полученное значение будет зависеть от метода измерения и условий, используемых при применении метода;
- если значение присвоено, могут быть указаны условия, при которых это присвоение является действительным;
- в случае присвоения или измерения условия, при которых значение является действительным, выражаются в виде набора количественных и качественных данных, которые формируют среду данных.

**НАПРИМЕР**, условия окружающей среды для измерения могут быть выражены как "воздух в помещении" (качественное состояние) или воздух при количественных условиях, указанных как 20 градусов Цельсия и давление в 1 атмосферу.

Условия метода измерения могут поддерживаться постоянными на протяжении всего измерения. В качестве альтернативы, некоторые условия могут изменяться независимо от других условий для получения набора связанных свойств.

Не все значения свойств должны быть выражены количественно, т.е. числовыми значениями. Значения также могут быть выражены качественно, т.е. с помощью описания.

**НАПРИМЕР**, цвет, поддающийся количественному выражению, в основном описывается качественно такими словами, как "красный", "эгейский синий", "серый металлик" и т.д.

===========================================================================================================


The subjects of the material_property_representation_schema are the representations of engineering properties and of the conditions under which these property representations are valid.

The following are the fundamental concepts and assumptions related to the representation of engineering properties:

multiple representations of a property are possible including the use of numeric values, parametric or fundamental equations, graphical representations and non-numeric values;
NOTE    The distinction between a concept and the representation of a concept is described in ISO 10303-43

the value of a property may be assigned or measured;
if the value is measured, the resulting value will depend on the method of measurement and on the conditions used in applying the method;
if the value is assigned, the conditions under which that assignment is valid may be specified;
in the case of either assignment or measurement, the conditions under which the value is valid are expressed as a set of quantitative and qualitative data which form the data environment.
EXAMPLE    The ambient conditions for a measurement may be expressed as 'room air' (a qualitative condition) or air at the quantitative conditions specified as 20 degrees Celsius and 1 atmosphere pressure.

The conditions of the measurement method may be maintained as constant throughout the measurement. Alternatively, some conditions may be varied independently of other conditions to provide a set of related properties.

Not all values of properties need to be expressed quantitatively, i.e. by numerical values. Values may also be expressed qualitatively, i.e. by a description.

EXAMPLE    Colour, through expressible quantitatively, is mostly described qualitatively by words such as 'red', 'Aegean blue', 'metallic grey', etc.