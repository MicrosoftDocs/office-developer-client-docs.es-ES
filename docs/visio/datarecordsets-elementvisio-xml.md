---
title: Elemento DataRecordSets (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Contiene todos los elementos DataRecordset del documento.
ms.openlocfilehash: efa7d58eabc1b1192862dbbe090ddd5008947c1d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542446"
---
# <a name="datarecordsets-element-visio-xml"></a>Elemento DataRecordSets (Visio XML)

Contiene todos los **elementos DataRecordset** del documento. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Contiene todos los **elementos DataRecordset** del documento.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Identificador del conjunto de registros de datos activo en la ventana **Datos** externos cuando se cierra la ventana, de modo que se pueda restaurar la próxima vez que se abra la ventana.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|DataWindowOrder  <br/> |xsd:string  <br/> |opcional  <br/> |El orden de los conjuntos de registros de datos que se muestran en las pestañas de la **ventana Datos** externos. Una lista ordenada de los IDs del conjunto de registros de datos, separados por punto y coma.  <br/> |Valores del tipo xsd:string.  <br/> |
|NextID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El siguiente identificador disponible para un nuevo conjunto de registros de datos.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

