---
title: Elemento RowMap (complexType DataRecordSet_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Asigna una fila de un conjunto de registros de datos a una forma.
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332518"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a>Elemento RowMap (complexType DataRecordSet_Type) ("XML" de Visio)

Asigna una fila de un conjunto de registros de datos a una forma.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

****

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |IDENTIFICADOR de página de la forma vinculada a los datos de la fila del conjunto de registros de datos identificado por **ROWID**.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Pseudocolumna  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |IDENTIFICADOR de fila de la fila, único dentro del conjunto de registros de datos.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|ShapeID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |IDENTIFICADOR de la forma vinculada a los datos de la fila del conjunto de registros de datos identificado por **ROWID**.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
   

