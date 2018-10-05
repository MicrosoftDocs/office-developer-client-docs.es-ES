---
title: Elemento de RefreshableData (PublishSettings_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9a3b9d5a-fcba-eb18-3199-bd5a7f889af8
description: Especifica si un conjunto de registros es actualizable mediante servicios de Visio en Microsoft SharePoint Server 2013.
ms.openlocfilehash: b402e2c9d65bf868c0ac33c782b87857ab6aed75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384877"
---
# <a name="refreshabledata-element-publishsettingstype-complextype-visio-xml"></a>Elemento de RefreshableData (PublishSettings_Type complexType) ('XML de Visio')

Especifica si un conjunto de registros es actualizable mediante servicios de Visio en Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RefreshableData_Type](refreshabledata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:element name="RefreshableData" type="RefreshableData_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[PublishSettings](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |Especifica la configuración que se usa cuando se abre el diagrama mediante servicios de Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El identificador de un objeto recordset.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

