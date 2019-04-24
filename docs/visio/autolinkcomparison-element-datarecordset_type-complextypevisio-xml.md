---
title: Elemento AutoLinkComparison (complexType DataRecordSet_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Define una regla que compara una columna del elemento DataRecordset principal con un elemento de datos de formas de la última acción de vinculación automática correcta realizada en la interfaz de usuario.
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338321"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>Elemento AutoLinkComparison (complexType DataRecordSet_Type) ("XML" de Visio)

Define una regla que compara una columna del elemento **DataRecordset** principal con un elemento de datos de formas de la última acción de vinculación automática correcta realizada en la interfaz de usuario. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Especifica un conjunto de registros y el enlace de datos entre ese conjunto de registros y formas en las páginas del dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |xsd: String  <br/> |necesario  <br/> |Corresponde a un nombre de columna en el objeto Recordset de ADO.  <br/> |Valores del tipo xsd: String.  <br/> |
|ContextType  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |Especifica las propiedades del grupo o la forma que se va a usar para la comparación. Los valores posibles se muestran en la tabla siguiente.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|ContextTypeLabel  <br/> |xsd: String  <br/> |opcional  <br/> |Si el valor de ContextType es 2 o 3, este atributo es necesario para definir una comparación. Para ContextType = 2, ContextTypeLabel debe ser la etiqueta del elemento de datos de formas y si **ContextType** = 3, ContextTypeLabel debe ser el nombre de fila local.  <br/> |Valores del tipo xsd: String.  <br/> |
   

