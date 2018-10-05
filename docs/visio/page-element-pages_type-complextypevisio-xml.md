---
title: Elemento de página (Pages_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Contiene elementos que definen una página del documento.
ms.openlocfilehash: 800e4ab2c6446ab298747f0492800000bb44cca3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398013"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Elemento de página (Pages_Type complexType) ('XML de Visio')

Contiene elementos que definen una página del documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Pages.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Contiene los elementos de **página** para el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contiene elementos que definen la hoja de página de un elemento de **página** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Fondo  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Una marca que indica si la página es una página de fondo.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|BackPage  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador de página de fondo de la página.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Indica si el nombre se ha personalizado por el usuario.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|IsCustomNameU  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Indica si el nombre universal se ha personalizado por el usuario.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre del elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre universal del elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El identificador de revisor asociado con la superposición de marcado.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd: Double  <br/> |opcional  <br/> |**ViewCenterX** y **ViewCenterY** especifican un punto central en una página que se supone una nueva vista (ventana) cuando se abre inicialmente.  <br/> |Valores del tipo XSD: Double.  <br/> |
|ViewCenterY  <br/> |xsd: Double  <br/> |opcional  <br/> |**ViewCenterX** y **ViewCenterY** especifican un punto central en una página que se supone una nueva vista (ventana) cuando se abre inicialmente.  <br/> |Valores del tipo XSD: Double.  <br/> |
|ViewScale  <br/> |xsd: Double  <br/> |opcional  <br/> |El factor de ampliación predeterminado para usar cuando se abre una nueva vista (ventana) de la página. Por ejemplo, 1 = 100%; 1,5 = 150% y así sucesivamente.  <br/> |Valores del tipo XSD: Double.  <br/> |
   

