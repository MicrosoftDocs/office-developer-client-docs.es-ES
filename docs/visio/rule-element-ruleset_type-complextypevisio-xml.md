---
title: Elemento rule (RuleSet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Representa una regla de validación única en un conjunto de reglas de validación de diagramas.
ms.openlocfilehash: feae283c624bdece98dbc1136b0fe8765d911e12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823065"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a>Elemento rule (RuleSet_Type complexType) ('XML de Visio')

Representa una regla de validación única en un conjunto de reglas de validación de diagramas.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Validation.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Conjuntos de reglas](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Representa un conjunto de reglas de validación del diagrama.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Especifica la expresión lógica que determina si se debe aplicar la regla de validación para un objeto de destino.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Especifica la expresión lógica que determina si el objeto de destino satisface la regla de validación.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Category  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el texto que aparece en la columna de **categoría** de la ventana problemas. El valor predeterminado es una cadena vacía.  <br/> |Valores del tipo XSD: String.  <br/> |
|Descripción  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica la descripción de la regla de validación que aparece en la interfaz de usuario. Valor predeterminado es "Unknown".  <br/> |Valores del tipo XSD: String.  <br/> |
|id.  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica el identificador único para la regla de validación.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Pasa por alto  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica si la regla de validación actualmente se omite. Valor predeterminado es False.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|NameU  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica el nombre universal de la regla de validación.  <br/> |Valores del tipo XSD: String.  <br/> |
|RuleTarget  <br/> |xsd: int  <br/> |opcional  <br/> |Especifica el tipo de objeto al que se aplica la regla de validación.  <br/> |Valores del tipo XSD: int.  <br/> |
   

