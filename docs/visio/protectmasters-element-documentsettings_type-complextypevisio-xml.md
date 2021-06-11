---
title: Elemento ProtectMasters (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Especifica si el usuario no puede crear, editar o eliminar formas maestras. El usuario todavía puede crear nuevas formas a partir de una forma maestra, independientemente de esta configuración.
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540696"
---
# <a name="protectmasters-element-documentsettings_type-complextype-visio-xml"></a>Elemento ProtectMasters (DocumentSettings_Type complexType) (Visio XML)

Especifica si el usuario no puede crear, editar o eliminar formas maestras. El usuario todavía puede crear nuevas formas a partir de una forma maestra, independientemente de esta configuración. 
  
El intervalo de valores posibles para este elemento es '0' o '1'. Un valor de "0" indica que los usuarios pueden crear, editar o eliminar formas maestras. Un valor de "1" indica que los usuarios no pueden crear, editar ni eliminar formas maestras.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contiene elementos que especifican la configuración del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

Ninguno.
  

