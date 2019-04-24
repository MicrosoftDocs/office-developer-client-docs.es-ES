---
title: Formato de persistencia XML
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7825d55c6f0c2f900f61a325265dce048f965e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308284"
---
# <a name="xml-persistence-format"></a>Formato de persistencia XML

**Se aplica a:** Access 2013, Office 2013

## <a name="xml-persistence-format"></a>Formato de persistencia XML

ADO utiliza la codificación UTF-8 para la secuencia XML que almacena.

El formato XML de ADO se divide en dos secciones, una sección de esquema seguida de otra de datos. A continuación, se proporciona un ejemplo de archivo XML para la tabla Shippers de la base de datos Neptuno. Después del ejemplo, se analizan diversas partes del XML.

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

El esquema muestra las declaraciones de espacio de nombres, las secciones de esquema y de datos. La sección de esquema contiene definiciones para fila, ShipperID, CompanyName y Phone.

Las definiciones de esquema cumplen la especificación XML-Data y se pueden validar totalmente (aunque la validación no funcionará en Internet Explorer 5). Puede ver esta especificación en [Notas sobre W3C XMLData](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data es actualmente el único formato de esquema admitido para persistencia de **conjuntos de registros**.

La sección de datos tiene tres filas que contienen información sobre compañías de envío. Para un conjunto de filas vacío, la sección de datos puede estar vacía `<rs:data>` , pero las etiquetas deben estar presentes. Sin datos, puede escribir la etiqueta abreviada simplemente `<rs:data>`como. Cualquier etiqueta con el prefijo "rs" indica que se encuentra en el espacio de nombres definido por urn:schemas-microsoft-com:rowset. La definición completa de este esquema se muestra en el apéndice de este documento.

## <a name="xml-persistence-format"></a>Formato de persistencia XML

ADO utiliza la codificación UTF-8 para la secuencia XML que almacena.

El formato XML de ADO se divide en dos secciones, una sección de esquema seguida de otra de datos. A continuación, se proporciona un ejemplo de archivo XML para la tabla Shippers de la base de datos Neptuno. Después del ejemplo, se analizan diversas partes del XML.

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

El esquema muestra las declaraciones de espacio de nombres, las secciones de esquema y de datos. La sección de esquema contiene definiciones para fila, ShipperID, CompanyName y Phone.

Las definiciones de esquema cumplen la especificación XML-Data y se pueden validar totalmente (aunque la validación no funcionará en Internet Explorer 5). Puede ver esta especificación en [Notas sobre W3C XMLData](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data es actualmente el único formato de esquema admitido para persistencia de **conjuntos de registros**.

La sección de datos tiene tres filas que contienen información sobre compañías de envío. Para un conjunto de filas vacío, la sección de datos puede estar vacía `<rs:data>` , pero las etiquetas deben estar presentes. Sin datos, puede escribir la etiqueta abreviada simplemente `<rs:data>`como. Cualquier etiqueta con el prefijo "rs" indica que se encuentra en el espacio de nombres definido por urn:schemas-microsoft-com:rowset. La definición completa de este esquema se muestra en el apéndice de este documento.

