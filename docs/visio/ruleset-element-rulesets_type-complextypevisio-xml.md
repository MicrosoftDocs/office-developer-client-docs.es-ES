---
title: Elemento RuleSet (RuleSets_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Representa un conjunto de reglas de validación de diagrama.
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541641"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a>Elemento RuleSet (RuleSets_Type complexType) (XML de Visio)

Representa un conjunto de reglas de validación de diagrama.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Incluye un **elemento RuleSet** para cada conjunto de reglas de validación del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Representa una regla de validación única en un conjunto de reglas de validación de diagramas.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Especifica las propiedades del conjunto de reglas.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Description  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica la descripción que aparece en la interfaz de usuario para el conjunto de reglas de validación. El valor predeterminado es una cadena vacía.  <br/> |Valores del tipo xsd:string.  <br/> |
|Habilitado  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica si se comprueban las reglas del conjunto de reglas de validación especificado cuando se desencadena la validación para el documento actual. El valor predeterminado es TrueTrue.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica el identificador único del conjunto de reglas de validación.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Nombre  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica el nombre local del conjunto de reglas de validación. El valor predeterminado es el valor del atributo NameU.  <br/> |Valores del tipo xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |necesario  <br/> |Especifica el nombre universal del conjunto de reglas de validación.  <br/> |Valores del tipo xsd:string.  <br/> |
   

