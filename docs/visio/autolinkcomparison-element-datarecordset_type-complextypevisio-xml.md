---
title: Elemento de AutoLinkComparison (DataRecordSet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Define una regla que se compara una columna en el elemento de DataRecordset primario con un elemento de datos de formas de la última correcta automática vinculación acción realizada en la interfaz de usuario.
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385721"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>Elemento de AutoLinkComparison (DataRecordSet_Type complexType) ('XML de Visio')

Define una regla que se compara una columna en el elemento de **DataRecordset** primario con un elemento de datos de formas de la última correcta automática vinculación acción realizada en la interfaz de usuario. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Especifica un conjunto de registros y el enlace de datos entre ese conjunto de registros y las formas en las páginas de dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |xsd: String  <br/> |necesario  <br/> |Corresponde a un nombre de columna del objeto Recordset de ADO.  <br/> |Valores del tipo XSD: String.  <br/> |
|ContextType  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica las propiedades del grupo o forma que se va a utilizar para la comparación. Los valores posibles se muestran en la siguiente tabla.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ContextTypeLabel  <br/> |xsd: String  <br/> |opcional  <br/> |Si el valor de ContextType es 2 o 3, este atributo es necesario para definir una comparación. Para ContextType = 2, ContextTypeLabel debe ser la etiqueta del elemento de datos de forma y si **ContextType** = 3, ContextTypeLabel debe ser el nombre de fila local.  <br/> |Valores del tipo XSD: String.  <br/> |
   

