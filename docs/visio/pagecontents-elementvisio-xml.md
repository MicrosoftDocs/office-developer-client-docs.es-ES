---
title: Elemento PageContents (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Especifica la información sobre las formas de una página maestra o de dibujo de un dibujo.
ms.openlocfilehash: aec860f4135e15f18436dba50986b0ad0e6ee9e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334513"
---
# <a name="pagecontents-element-visio-xml"></a>Elemento PageContents (' Visio XML ')

Especifica la información sobre las formas de una página maestra o de dibujo de un dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica una colección de formas.  <br/> |
   
### <a name="attributes"></a>Atributos

Ninguno.
  

