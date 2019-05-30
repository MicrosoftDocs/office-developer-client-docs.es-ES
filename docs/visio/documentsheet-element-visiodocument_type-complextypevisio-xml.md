---
title: Elemento DocumentSheet (complexType VisioDocument_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Especifica una estructura DocumentSheet.
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540045"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a>Elemento DocumentSheet (complexType VisioDocument_Type) (XML de Visio)

Especifica una estructura DocumentSheet.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |El elemento raíz de un documento de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una celda en un DocumentSheet.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Describe si el usuario ha personalizado el nombre.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|IsCustomNameU  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Describe si el usuario ha personalizado el nombre universal.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre dependiente del idioma de DocumentSheet.  <br/> |Valores del tipo xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre independiente del idioma de DocumentSheet.  <br/> |Valores del tipo xsd: String.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |opcional  <br/> |String opcional. Un GUID (identificador único global) que identifica la forma.  <br/> |Valores del tipo xsd: String.  <br/> |
   

