---
title: Elemento de Windows ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contiene los elementos de la ventana de un documento.
ms.openlocfilehash: df4d4bc48db157bd05fd39177975c9dbeaa5de52
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386806"
---
# <a name="windows-element-visio-xml"></a>Elemento de Windows ('XML de Visio')

Contiene los elementos de la **ventana** de un documento. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Windows.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Representa una ventana abierta en una instancia de Microsoft Visio.
  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Propiedades ClientHeight  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Representa el alto de un área de presentación  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|ClientWidth  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Representa el ancho de un área de presentación  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
   

