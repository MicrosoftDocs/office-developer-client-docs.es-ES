---
title: Elemento ValidationProperties (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: Encapsula las propiedades relacionadas con la validación del documento.
ms.openlocfilehash: 35e6f3f13eecef826fdef0d664bba35fceb0e069
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538525"
---
# <a name="validationproperties-element-validation_type-complextype-visio-xml"></a>Elemento ValidationProperties (Validation_Type complexType) (Visio XML)

Encapsula las propiedades relacionadas con la validación del documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Validation](validation-elementvisio-xml.md) <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |Almacena información sobre la validación del diagrama para el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|LastValidated  <br/> |xsd:dateTime  <br/> |necesario  <br/> |Fecha y hora en que se validó por última vez el documento.  <br/> |Valores del tipo xsd:dateTime.  <br/> |
|ShowIgnored  <br/> |xsd:boolean  <br/> |necesario  <br/> |Especifica si se deben mostrar problemas de validación omitido en la ventana Problemas.  <br/> |Valores del tipo xsd:boolean.  <br/> |
   

