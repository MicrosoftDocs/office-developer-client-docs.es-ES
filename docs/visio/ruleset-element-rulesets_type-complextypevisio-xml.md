---
title: Elemento RuleSet (RuleSets_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Representa un conjunto de reglas de validación del diagrama.
ms.openlocfilehash: ae8fc52dd665e51f38c7eeae2f12ff778937d565
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823085"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a>Elemento RuleSet (RuleSets_Type complexType) ('XML de Visio')

Representa un conjunto de reglas de validación del diagrama.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Validation.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Conjuntos de reglas](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Incluye un elemento de **conjunto de reglas** para cada regla de validación establecida en el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Representa una regla de validación única en un conjunto de reglas de validación de diagramas.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Especifica las propiedades del conjunto de reglas.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Descripción  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica la descripción que aparece en la interfaz de usuario para el conjunto de reglas de validación. El valor predeterminado es una cadena vacía.  <br/> |Valores del tipo XSD: String.  <br/> |
|Habilitado  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica si se comprueban las reglas en el conjunto de reglas de validación especificado cuando se desencadena la validación para el documento actual. Valor predeterminado es True.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica el identificador único del conjunto de reglas de validación.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre local del conjunto de reglas de validación. El valor predeterminado es el valor del atributo de NameU.  <br/> |Valores del tipo XSD: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica el nombre universal del conjunto de reglas de validación.  <br/> |Valores del tipo XSD: String.  <br/> |
   

