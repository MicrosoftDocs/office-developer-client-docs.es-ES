---
title: Elemento AutoLinkComparison (DataRecordSet_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Define una regla que compara una columna del elemento Primario DataRecordset con un elemento de datos de formas de la última acción de vinculación automática realizada correctamente en la interfaz de usuario.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537874"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a>Elemento AutoLinkComparison (DataRecordSet_Type complexType) (XML de Visio)

Define una regla que compara una columna del elemento **DataRecordset** primario con un elemento de datos de formas de la última acción de vinculación automática realizada correctamente en la interfaz de usuario. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Especifica un conjunto de registros y el enlace de datos entre ese conjunto de registros y las formas de las páginas de dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |xsd:string  <br/> |necesario  <br/> |Corresponde a un nombre de columna del conjunto de registros de ADO.  <br/> |Valores del tipo xsd:string.  <br/> |
|ContextType  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica las propiedades del grupo o la forma que se usarán para la comparación. En la tabla siguiente se muestran los valores posibles.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ContextTypeLabel  <br/> |xsd:string  <br/> |opcional  <br/> |Si el valor de ContextType es 2 o 3, este atributo es necesario para definir una comparación. Para ContextType = 2, ContextTypeLabel debe ser la etiqueta del elemento de datos de formas y, si **ContextType** = 3, ContextTypeLabel debe ser el nombre de fila local.  <br/> |Valores del tipo xsd:string.  <br/> |
   

