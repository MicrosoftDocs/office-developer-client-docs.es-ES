---
title: Elemento PublishSettings (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Especifica la configuración que se usa cuando se abre el diagrama mediante Visio Services en Microsoft SharePoint Server 2013.
ms.openlocfilehash: 611dfe477228995bca6aedff27b468a2d57e7e85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541361"
---
# <a name="publishsettings-element-visiodocument_type-complextype-visio-xml"></a>Elemento PublishSettings (VisioDocument_Type complexType) (Visio XML)

Especifica la configuración que se usa cuando se abre el diagrama mediante Visio Services en Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Especifica las propiedades de un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[PublishedPage](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[PublishedPage_Type](publishedpage_type-complextypevisio-xml.md) <br/> |Especifica si una página de dibujo se puede ver en el explorador mediante Visio Servicios.  <br/> |
|[RefreshableData](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[RefreshableData_Type](refreshabledata_type-complextypevisio-xml.md) <br/> |Especifica si un conjunto de registros se puede actualizar mediante Visio Services.  <br/> |
   
### <a name="attributes"></a>Atributos

Ninguno.
  

