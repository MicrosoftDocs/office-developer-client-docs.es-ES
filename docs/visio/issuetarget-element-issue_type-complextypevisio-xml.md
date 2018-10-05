---
title: Elemento de IssueTarget (Issue_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Según el destino del elemento primario problema de validación, especifica la página, o la página y la forma, asociado con el problema de validación primario. Si el destino del problema de validación primario es un documento, IssueTarget especifica una página ni una forma.
ms.openlocfilehash: 74005bfb6035e32b7b34fdd5a8a5737813a562a0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385364"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a>Elemento de IssueTarget (Issue_Type complexType) ('XML de Visio')

Según el destino del elemento primario problema de validación, especifica la página, o la página y la forma, asociado con el problema de validación primario. Si el destino del problema de validación primario es un documento, **IssueTarget** especifica una página ni una forma. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Validation.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Problema](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Representa un problema de validación único en el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica el identificador único de la página que está asociada con el problema de validación primario. Si el destino es el documento, el valor de PageID puede ser 0xFFFFFFFF.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica el identificador único de la forma que está asociada con el problema de validación primario. Si el destino es una página o el documento, el valor de ShapeID puede ser 0xFFFFFFFF.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

