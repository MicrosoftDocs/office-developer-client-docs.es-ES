---
title: Elemento DataColumns (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contiene todos los elementos DataColumn de un conjunto de registros de datos.
ms.openlocfilehash: e42354076c5e3e34c118145e7ec7fcdbd4977372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541200"
---
# <a name="datacolumns-element-datarecordset_type-complextype-visio-xml"></a>Elemento DataColumns (DataRecordSet_Type complexType) (Visio XML)

Contiene todos los **elementos DataColumn** de un conjunto de registros de datos. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataColumn](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |Define cómo aparece una  columna de datos en la ventana Datos externos de la interfaz de usuario de Visio y clasifica los datos de la columna definiendo su tipo de datos y formato.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|SortAsc  <br/> |xsd:boolean  <br/> |opcional  <br/> |Columna en la que se ordenarán los datos.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|SortColumn  <br/> |xsd:string  <br/> |opcional  <br/> |Ordenar la columna **SortColumn** en orden ascendente (1) o descendente (0).  <br/> |Valores del tipo xsd:string.  <br/> |
   

