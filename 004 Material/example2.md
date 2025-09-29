2) Пластик для корпуса: диаграмма напряжение‑деформация в виде таблицы точек при 23 °C и скорости деформации 0,01 с⁻¹; модуль Юнга и ударная вязкость с указанием стандартов испытаний.

```console
ISO-10303-21;
HEADER;
FILE_DESCRIPTION(('Экспорт свойств пластика для корпуса'), '1');
FILE_NAME('plastic_case.stp','2025-09-25T16:46:00',('Author'),('Organization'),'','CAE_system','');
FILE_SCHEMA(('MATERIAL_PROPERTY_SCHEMA'));
ENDSEC;
DATA;
#10=MATERIAL('ABS','ABS пластик','ABS пластик для корпуса');
#20=PROPERTY_TABLE('Stress-Strain at 23C, rate 0.01 1/s',('Strain','Stress'),((0.0,0.0),(0.01,1.3),(0.02,2.6),(0.03,3.7),(0.04,4.8)));
#21=TEST_CONDITION('Temperature',23.0,'degC');
#22=TEST_CONDITION('Strain rate',0.01,'1/s');
#23=PROPERTY_TABLE_CONDITION(#20,#21);
#24=PROPERTY_TABLE_CONDITION(#20,#22);
#30=PROPERTY('Young_modulus',2100.0,'MPa');
#31=TEST_METHOD(#30,'ISO 527-2');
#40=PROPERTY('Impact_strength',28.5,'kJ/m2');
#41=TEST_METHOD(#40,'ISO 179');
#50=MATERIAL_PROPERTY_ASSOCIATION(#10,#20);
#51=MATERIAL_PROPERTY_ASSOCIATION(#10,#30);
#52=MATERIAL_PROPERTY_ASSOCIATION(#10,#40);
ENDSEC;
END-ISO-10303-21;
```

```xml
<iso_10303_28>
  <header>
    <file_description>Экспорт свойств пластика для корпуса</file_description>
    <file_name>plastic_case.xml</file_name>
    <author>Author</author>
    <organization>Organization</organization>
    <preprocessor_version>STEP-XML generator v1.0</preprocessor_version>
    <originating_system>CAE_application</originating_system>
    <creation_date>2025-09-25T16:48:00</creation_date>
  </header>
  <data>
    <material id="mat1">
      <name>ABS</name>
      <description>ABS пластик для корпуса</description>
    </material>
    <property_table id="pt1">
      <name>Stress-Strain Curve at 23 C and strain rate 0.01 1/s</name>
      <columns>
        <column>Strain</column>
        <column>Stress</column>
      </columns>
      <rows>
        <row><value>0.0</value><value>0.0</value></row>
        <row><value>0.01</value><value>1.3</value></row>
        <row><value>0.02</value><value>2.6</value></row>
        <row><value>0.03</value><value>3.7</value></row>
        <row><value>0.04</value><value>4.8</value></row>
      </rows>
      <test_conditions>
        <condition>
          <parameter>Temperature</parameter>
          <value>23</value>
          <unit>degC</unit>
        </condition>
        <condition>
          <parameter>Strain rate</parameter>
          <value>0.01</value>
          <unit>1/s</unit>
        </condition>
      </test_conditions>
      <reference>mat1</reference>
    </property_table>
    <property id="prop1">
      <name>Young's Modulus</name>
      <value>2100</value>
      <unit>MPa</unit>
      <test_method>ISO 527-2</test_method>
      <reference>mat1</reference>
    </property>
    <property id="prop2">
      <name>Impact Strength</name>
      <value>28.5</value>
      <unit>kJ/m2</unit>
      <test_method>ISO 179</test_method>
      <reference>mat1</reference>
    </property>
  </data>
</iso_10303_28>

```

```json
{
  "material": {
    "id": "mat1",
    "name": "ABS",
    "description": "ABS пластик для корпуса"
  },
  "propertyTable": {
    "id": "pt1",
    "name": "Stress-Strain Curve at 23C and strain rate 0.01 1/s",
    "columns": ["Strain", "Stress"],
    "rows": [
      [0.0, 0.0],
      [0.01, 1.3],
      [0.02, 2.6],
      [0.03, 3.7],
      [0.04, 4.8]
    ],
    "testConditions": [
      {"parameter": "Temperature", "value": 23, "unit": "degC"},
      {"parameter": "Strain rate", "value": 0.01, "unit": "1/s"}
    ],
    "reference": "mat1"
  },
  "properties": [
    {
      "id": "prop1",
      "name": "Young's Modulus",
      "value": 2100,
      "unit": "MPa",
      "testMethod": "ISO 527-2",
      "reference": "mat1"
    },
    {
      "id": "prop2",
      "name": "Impact Strength",
      "value": 28.5,
      "unit": "kJ/m2",
      "testMethod": "ISO 179",
      "reference": "mat1"
    }
  ]
}
```
