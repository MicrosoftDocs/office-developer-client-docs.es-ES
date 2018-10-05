---
title: Elemento de RowMap (DataRecordSet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Asigna una fila del conjunto de registros de datos a una forma.
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385315"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a>Elemento de RowMap (DataRecordSet_Type complexType) ('XML de Visio')

Asigna una fila del conjunto de registros de datos a una forma.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

****

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador de página de la forma vinculada a los datos en la fila del conjunto de registros de datos identificada por **RowID**.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|RowID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador de la fila, única en el conjunto de registros de datos.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador de la forma de la forma vinculada a los datos en la fila del conjunto de registros de datos identificada por **RowID**.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

