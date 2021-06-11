---
title: Elemento RuleSetFlags (RuleSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c18d3a84-2088-13f7-7b14-1f4c129537b4
description: Especifica las propiedades del conjunto de reglas.
ms.openlocfilehash: 03b94abb2d9bbe1f611671a4ac37053747a486fb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541599"
---
# <a name="rulesetflags-element-ruleset_type-complextype-visio-xml"></a>Elemento RuleSetFlags (RuleSet_Type complexType) (Visio XML)

Especifica las propiedades del conjunto de reglas.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RuleSetFlags" type="RuleSetFlags_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RuleSet](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Representa un conjunto de reglas de validación de diagramas.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Hidden  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica si el conjunto de reglas aparece en la lista Reglas para comprobar.  <br/> |Valores del tipo xsd:boolean.  <br/> |
   

