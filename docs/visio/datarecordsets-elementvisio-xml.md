---
title: Elemento DataRecordsets (' XML ' de Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Contiene todos los elementos DataRecordset del documento.
ms.openlocfilehash: 7730e55f0025181db193a1e64226e879f9072e90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360329"
---
# <a name="datarecordsets-element-visio-xml"></a>Elemento DataRecordsets (' XML ' de Visio ')

Contiene todos los elementos **DataRecordset** del documento. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Contiene todos los elementos **DataRecordset** del documento.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |IDENTIFICADOR del conjunto de registros de datos activo de la ventana **datos externos** cuando se cierre la ventana, de modo que se pueda restaurar la próxima vez que se abra la ventana.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|DataWindowOrder  <br/> |xsd: String  <br/> |opcional  <br/> |Orden de los conjuntos de registros de datos que se muestran en las pestañas de la ventana **datos externos** . Una lista ordenada de identificadores de conjunto de registros de datos, separados por punto y coma.  <br/> |Valores del tipo xsd: String.  <br/> |
|NextID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |El siguiente identificador disponible para un nuevo conjunto de registros de datos.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
   

