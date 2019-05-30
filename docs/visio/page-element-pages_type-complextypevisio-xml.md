---
title: Elemento Page (Pages_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Contiene los elementos que definen una página en el documento.
ms.openlocfilehash: f32cf3ed7bbf1e68ddca3fc8f5a1c50ce45fe73e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538028"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Elemento Page (Pages_Type complexType) (XML de Visio)

Contiene los elementos que definen una página en el documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Pages. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Contiene los elementos de **Página** del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contiene elementos que definen la hoja de página de un elemento de **Página** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Fondo  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Marca que indica si la página es una página de fondo.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|BackPage  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |El identificador de la página de fondo de esta página.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |IDENTIFICADOR único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Indica si el usuario ha personalizado el nombre.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|IsCustomNameU  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Indica si el usuario ha personalizado el nombre universal.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |Nombre del elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |Nombre universal del elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|ReviewerID  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |IDENTIFICADOR del revisor asociado a la revisión superpuesta.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd: Double  <br/> |opcional  <br/> |**ViewCenterX** y **ViewCenterY** especifican un punto central en una página que una nueva vista (ventana) da por sentado cuando se abre inicialmente.  <br/> |Valores del tipo xsd: Double.  <br/> |
|ViewCenterY  <br/> |xsd: Double  <br/> |opcional  <br/> |**ViewCenterX** y **ViewCenterY** especifican un punto central en una página que una nueva vista (ventana) da por sentado cuando se abre inicialmente.  <br/> |Valores del tipo xsd: Double.  <br/> |
|ViewScale  <br/> |xsd: Double  <br/> |opcional  <br/> |El factor de ampliación predeterminado que se debe usar cuando se abre una nueva vista (ventana) de la página. Por ejemplo, 1 = 100%; 1,5 = 150%, y así sucesivamente.  <br/> |Valores del tipo xsd: Double.  <br/> |
   

