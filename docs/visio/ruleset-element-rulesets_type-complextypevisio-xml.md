---
title: Elemento RuleSet (RuleSets_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Representa un conjunto de reglas de validación de diagrama.
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318917"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a>Elemento RuleSet (RuleSets_Type complexType) ("XML" de Visio)

Representa un conjunto de reglas de validación de diagrama.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Validation. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Incluye un elemento **ruleset** para cada conjunto de reglas de validación en el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Representa una regla de validación única en un conjunto de reglas de validación de diagramas.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Especifica las propiedades del conjunto de reglas.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Descripción  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica la descripción que aparece en la interfaz de usuario del conjunto de reglas de validación. El valor predeterminado es una cadena vacía.  <br/> |Valores del tipo xsd: String.  <br/> |
|Habilitado  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Especifica si se activan las reglas del conjunto de reglas de validación especificado cuando se desencadena la validación para el documento actual. El valor predeterminado es TrueTrue.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |Especifica el identificador único del conjunto de reglas de validación.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre local del conjunto de reglas de validación. El valor predeterminado del atributo NameU es.  <br/> |Valores del tipo xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica el nombre universal del conjunto de reglas de validación.  <br/> |Valores del tipo xsd: String.  <br/> |
   

