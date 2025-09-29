1) Болт из стали 40Х: материал — «40Х по ГОСТ …», свойства — предел прочности 800 МПа при 20 °C по методу ISO …, твёрдость 28–32 HRC, плотность 7,85 г/см³; всё с единицами, методами и ссылкой на сертификат партии.

```console
ISO-10303-21;
HEADER;
FILE_DESCRIPTION(('Экспорт свойств материала болта'), '1');
FILE_NAME('bolt_40X.step','2025-09-25T16:38:00',('Author'),('Organization'),'','CAD_application','');
FILE_SCHEMA(('MATERIAL_PROPERTY_SCHEMA'));
ENDSEC;
DATA;
#10=MATERIAL('40X','Steel to GOST ...', 'Steel grade 40X as per GOST ... standard');
#20=PROPERTY('Tensile strength',800.0,'MPa');
#21=PROPERTY('Hardness',28.0,'HRC');
#22=PROPERTY('Hardness',32.0,'HRC');
#23=PROPERTY('Density',7.85,'g/cm3');
#30=PROPERTY_DEFINITION('Tensile strength at 20C','According to ISO ...',#20);
#31=PROPERTY_DEFINITION('Hardness range 28-32 HRC','Measured per ISO ...',#21,#22);
#32=PROPERTY_DEFINITION('Density','Reference handbook',#23);
#40=MATERIAL_PROPERTY_ASSOCIATION(#10,#30);
#41=MATERIAL_PROPERTY_ASSOCIATION(#10,#31);
#42=MATERIAL_PROPERTY_ASSOCIATION(#10,#32);
#50=DOCUMENT('Certificate of batch', 'Sertifikat-123-45', 'https://certs.example/bolt-40x-cert.pdf');
#60=DOCUMENT_ASSOCIATION(#10,#50);
ENDSEC;
END-ISO-10303-21;
```

```xml
<iso_10303_28>
  <header>
    <file_description>Экспорт свойств материала болта</file_description>
    <file_name>bolt_40x.xml</file_name>
    <author>Author</author>
    <organization>Organization</organization>
    <preprocessor_version>STEP-XML generator v1.0</preprocessor_version>
    <originating_system>CAD_application</originating_system>
    <creation_date>2025-09-25T16:42:00</creation_date>
  </header>
  <data>
    <material id="mat1">
      <name>40X</name>
      <standard>GOST ...</standard>
      <description>Steel 40X as per GOST ... standard</description>
    </material>
    <property id="prop1">
      <name>Tensile strength</name>
      <value>800</value>
      <unit>MPa</unit>
      <test_condition>
        <temperature>20</temperature>
        <unit>degC</unit>
        <method>ISO ...</method>
      </test_condition>
      <reference>mat1</reference>
    </property>
    <property id="prop2">
      <name>Hardness</name>
      <value_min>28</value_min>
      <value_max>32</value_max>
      <unit>HRC</unit>
      <method>ISO ...</method>
      <reference>mat1</reference>
    </property>
    <property id="prop3">
      <name>Density</name>
      <value>7.85</value>
      <unit>g/cm3</unit>
      <reference>mat1</reference>
    </property>
    <document id="doc1">
      <name>Certificate of batch</name>
      <number>Sertifikat-123-45</number>
      <url>https://certs.example/bolt-40x-cert.pdf</url>
      <reference>mat1</reference>
    </document>
  </data>
</iso_10303_28>
```

```json
{
  "material": {
    "id": "mat1",
    "name": "40Х",
    "standard": "GOST ...",
    "description": "Сталь 40Х по ГОСТ ..."
  },
  "properties": [
    {
      "id": "prop1",
      "name": "Tensile strength",
      "value": 800,
      "unit": "MPa",
      "testCondition": {
        "temperature": 20,
        "unit": "degC"
      },
      "testMethod": "ISO ..."
    },
    {
      "id": "prop2",
      "name": "Hardness",
      "valueRange": {
        "min": 28,
        "max": 32
      },
      "unit": "HRC",
      "testMethod": "ISO ..."
    },
    {
      "id": "prop3",
      "name": "Density",
      "value": 7.85,
      "unit": "g/cm3"
    }
  ],
  "certificate": {
    "type": "Batch certificate",
    "id": "cert12345",
    "url": "https://certs.example/bolt-40x-cert.pdf"
  }
}
```
