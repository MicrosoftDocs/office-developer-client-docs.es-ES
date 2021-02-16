---
title: Elemento Rule (RuleSet_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Representa una regla de validación única en un conjunto de reglas de validación de diagramas.
ms.openlocfilehash: 0d848ce3309d7dfc5a89b201be30ce060ec6f88f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541711"
---
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a>Elemento Rule (RuleSet_Type complexType) (XML de Visio)

Representa una regla de validación única en un conjunto de reglas de validación de diagramas.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RuleSet](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Representa un conjunto de reglas de validación de diagrama.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Especifica la expresión lógica que determina si la regla de validación se debe aplicar a un objeto de destino.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Especifica la expresión lógica que determina si el objeto de destino cumple la regla de validación.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Categoría  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica el texto que se muestra en la columna **Categoría** de la ventana Problemas. El valor predeterminado es una cadena vacía.  <br/> |Valores del tipo xsd:string.  <br/> |
|Description  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica la descripción de la regla de validación que aparece en la interfaz de usuario. El valor predeterminado es "Unknown".  <br/> |Valores del tipo xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica el identificador único de la regla de validación.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Omitido  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica si la regla de validación se omite actualmente. El valor predeterminado es False.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|NameU  <br/> |xsd:string  <br/> |necesario  <br/> |Especifica el nombre universal de la regla de validación.  <br/> |Valores del tipo xsd:string.  <br/> |
|RuleTarget  <br/> |xsd:int  <br/> |opcional  <br/> |Especifica el tipo de objeto al que se aplica la regla de validación.  <br/> |Valores del tipo xsd:int.  <br/> |
   

