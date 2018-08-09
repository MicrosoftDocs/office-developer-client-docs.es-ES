---
title: Elemento de PublishedPage (PublishSettings_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Especifica si una página de dibujo está visible en el explorador con los servicios de Visio en Microsoft SharePoint Server 2013.
ms.openlocfilehash: 5cdbb03aaac3393c16c6ed0169842153374f668e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822882"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a>Elemento de PublishedPage (PublishSettings_Type complexType) ('XML de Visio')

Especifica si una página de dibujo está visible en el explorador con los servicios de Visio en Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PublishedPage_Type](publishedpage_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[PublishSettings](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |Especifica la configuración que se usa cuando se abre el diagrama mediante servicios de Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El identificador de una página de dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

