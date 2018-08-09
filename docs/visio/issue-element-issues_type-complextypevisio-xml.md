---
title: Elemento de problema (Issues_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Representa un problema de validación único en el documento.
ms.openlocfilehash: 904b42c969bdf97fcfa1e34bad97f73242b17cc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822387"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a>Elemento de problema (Issues_Type complexType) ('XML de Visio')

Representa un problema de validación único en el documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Validation.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Problemas](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Issues_Type](issues_type-complextypevisio-xml.md) <br/> |Contiene todos los elementos de **problema** para el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[IssueTarget](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |Según el destino del elemento primario problema de validación, especifica la página, o la página y la forma, asociado con el problema de validación primario.  <br/> |
|[RuleInfo](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |Especifica información acerca de la regla de validación que el problema de validación primario pertenece a.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica el identificador único del problema de validación.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Pasa por alto  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica información acerca de la regla de validación que el problema de validación primario pertenece a.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
   

