---
title: Elemento RuleTest (Rule_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cb95b34-3ce0-07a5-5d57-8ac9b0570b9a
description: Especifica la expresión lógica que determina si el objeto de destino cumple la regla de validación.
ms.openlocfilehash: bb1f0cf9b3f712903f6e45d6d09f96607089f920
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541522"
---
# <a name="ruletest-element-rule_type-complextype-visio-xml"></a>Elemento RuleTest (Rule_Type complexType) (Visio XML)

Especifica la expresión lógica que determina si el objeto de destino cumple la regla de validación.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RuleTest" type="RuleTest_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Representa una regla de validación única en un conjunto de reglas de validación de diagramas.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Fórmula  <br/> |xsd:string  <br/> |opcional  <br/> |Representa la fórmula del elemento.  <br/> |Valores de xsd:string.  <br/> |
   

