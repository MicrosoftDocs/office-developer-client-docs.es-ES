---
title: Elemento DataRecordSets ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Contiene todos los elementos de DataRecordset en el documento.
ms.openlocfilehash: 205c4d963f111490698627040c190f322f2f36a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821923"
---
# <a name="datarecordsets-element-visio-xml"></a>Elemento DataRecordSets ('XML de Visio')

Contiene todos los elementos de **DataRecordset** en el documento. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Contiene todos los elementos de **DataRecordset** en el documento.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador del conjunto de registros de datos activo en la ventana **Datos externos** cuando la ventana se cierra, por lo que se puede restaura la próxima vez que la ventana se abre.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DataWindowOrder  <br/> |xsd: String  <br/> |opcional  <br/> |El orden de los conjuntos de registros de datos que se muestran en las fichas de la ventana **Datos externos** . Una lista ordenada de los identificadores de conjunto de registros de datos, separados por punto y coma.  <br/> |Valores del tipo XSD: String.  <br/> |
|NextID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El siguiente identificador disponible para un nuevo conjunto de registros de datos.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

