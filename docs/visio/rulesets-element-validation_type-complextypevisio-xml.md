---
title: Elemento RuleSets (Validation_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Incluye un elemento de conjunto de reglas para cada regla de validación establecida en el documento.
ms.openlocfilehash: 84d64a8539f1b83c16a96a61ea68e9b2660c9036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823091"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a>Elemento RuleSets (Validation_Type complexType) ('XML de Visio')

Incluye un elemento de **conjunto de reglas** para cada regla de validación establecida en el documento. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Validation.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Validación](validation-elementvisio-xml.md) <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |Almacena información sobre la validación del diagrama para el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Conjuntos de reglas](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Representa un conjunto de reglas de validación del diagrama.  <br/> |
   
### <a name="attributes"></a>Atributos

Ninguno.
  

