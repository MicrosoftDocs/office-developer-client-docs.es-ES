---
title: Elemento IssueTarget (complexType Issue_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Según el destino del problema de validación principal, especifica la página, o bien la página y la forma, asociadas con el problema de validación principal. Si el destino del problema de validación principal es un documento, IssueTarget no especifica ni una página ni una forma.
ms.openlocfilehash: 74005bfb6035e32b7b34fdd5a8a5737813a562a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332525"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a>Elemento IssueTarget (complexType Issue_Type) ("XML" de Visio)

Según el destino del problema de validación principal, especifica la página, o bien la página y la forma, asociadas con el problema de validación principal. Si el destino del problema de validación principal es un documento, **IssueTarget** no especifica ni una página ni una forma. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Validation. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Problema](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Representa un único problema de validación en el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |Especifica el identificador único de la página que está asociado con el problema de validación primario. Si el destino es el documento, el valor de PageID puede ser 0xFFFFFFFF.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|ShapeID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |Especifica el identificador único de la forma asociada con el problema de validación primario. Si el destino es el documento o una página, el valor de ShapeID puede ser 0xFFFFFFFF.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
   

