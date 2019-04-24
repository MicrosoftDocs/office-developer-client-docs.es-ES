---
title: Elemento Solution (complexType Solutions_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Especifica una instancia de XML de solución almacenada en el dibujo.
ms.openlocfilehash: bb3cd512ff6109467c9d6465ba72c764d83abf96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335269"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a>Elemento Solution (complexType Solutions_Type) ("XML" de Visio)

Especifica una instancia de XML de solución almacenada en el dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Solutions. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Soluciones](solutions-elementvisio-xml.md) <br/> |[Solutions_Type](solutions_type-complextypevisio-xml.md) <br/> |Almacena las propiedades de las soluciones almacenadas en el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[REL](rel-element-solution_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |Especifica la relación con un elemento con el XML de la solución asociado a esta solución.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Nombre  <br/> |xsd: String  <br/> |necesario  <br/> |Nombre de la solución.  <br/> |Valores del tipo xsd: String.  <br/> |
   

