---
title: Conectar el elemento (Connects_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: "\n			Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.\n"
ms.openlocfilehash: 1bd3e1f006afe8d5bbb698e0b3a2179b74728315
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821844"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Conectar el elemento (Connects_Type complexType) ('XML de Visio')


			Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.

  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |página # .xml, master # .xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd: String  <br/> |opcional  <br/> |La celda desde la que se origina una conexión.  <br/> |Valores del tipo XSD: String.  <br/> |
|FromPart  <br/> |xsd: int  <br/> |opcional  <br/> |La parte de una forma desde la que se origina una conexión.  <br/> |Valores del tipo XSD: int.  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El identificador de la forma desde la que se originan una conexión o conexiones.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ToCell  <br/> |xsd: String  <br/> |opcional  <br/> |La celda a la que se realiza una conexión.  <br/> |Valores del tipo XSD: String.  <br/> |
|ToPart  <br/> |xsd: int  <br/> |opcional  <br/> |La parte de una forma a la que se realiza una conexión.  <br/> |Valores del tipo XSD: int.  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El identificador de la forma a la que se realizan una o más conexiones.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

