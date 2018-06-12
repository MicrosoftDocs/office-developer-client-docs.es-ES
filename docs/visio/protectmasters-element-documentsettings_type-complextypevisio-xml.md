---
title: Elemento de ProtectMasters (DocumentSettings_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Especifica si el usuario impide crear, editar o eliminar formas de patrón. El usuario puede crear nuevas formas de una forma de patrón, independientemente de esta configuración.
ms.openlocfilehash: cb576f267e076b06f2088ce53a18e9af36a46b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822865"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a>Elemento de ProtectMasters (DocumentSettings_Type complexType) ('XML de Visio')

Especifica si el usuario impide crear, editar o eliminar formas de patrón. El usuario puede crear nuevas formas de una forma de patrón, independientemente de esta configuración. 
  
El intervalo de valores posibles para este elemento es '0' o '1'. Un valor de '0' indica que los usuarios pueden crear, editar o eliminar formas de patrón. Un valor de '1' indica que los usuarios no pueden crear, modificar o eliminar formas de patrón.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contiene elementos que especifican la configuración de documentos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

Ninguno.
  

