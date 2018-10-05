---
title: Elemento DocumentSheet (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Especifica una estructura DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383467"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a>Elemento DocumentSheet (VisioDocument_Type complexType) ('XML de Visio')

Especifica una estructura DocumentSheet.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |El elemento raíz de un documento de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una celda en un DocumentSheet.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Describe si el nombre se ha personalizado por el usuario.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|IsCustomNameU  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Describe si se ha personalizado el nombre universal por el usuario.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre dependen del idioma de la DocumentSheet.  <br/> |Valores del tipo XSD: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre independiente del idioma de la DocumentSheet.  <br/> |Valores del tipo XSD: String.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |opcional  <br/> |String opcional. Un GUID (identificador único global) que identifica la forma.  <br/> |Valores del tipo XSD: String.  <br/> |
   

