---
title: Elemento de DataConnection (DataConnections_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Resume la comunicación entre uno o varios elementos de DataRecordset y un origen de datos no XML.
ms.openlocfilehash: 74e15795e023517263d9b79e9f19557653e4e939
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821928"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>Elemento de DataConnection (DataConnections_Type complexType) ('XML de Visio')

Resume la comunicación entre uno o varios elementos de **DataRecordset** y un origen de datos no XML. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Connections.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Contiene los elementos de **DataConnection** para el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |Boolean con tipo  <br/> |opcional  <br/> |El valor predeterminado es false. Para obtener más información, vea los Comentarios.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|Comando  <br/> |xsd: String  <br/> |opcional  <br/> |La cadena de comando utilizada para consultar el origen de datos.  <br/> |Valores del tipo XSD: String.  <br/> |
|ConnectionString  <br/> |xsd: String  <br/> |opcional  <br/> |La cadena de conexión que define los parámetros necesarios para conectarse a un origen de datos.  <br/> |Valores del tipo XSD: String.  <br/> |
|FileName  <br/> |xsd: String  <br/> |necesario  <br/> |El nombre del archivo de conexión. Para obtener más información, vea los Comentarios.  <br/> |Valores del tipo XSD: String.  <br/> |
|FriendlyName  <br/> |xsd: String  <br/> |opcional  <br/> |Un nombre proporcionado por el usuario para la conexión de datos.  <br/> |Valores del tipo XSD: String.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador asignado por Visio para una conexión determinada, única dentro del documento.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |El tiempo de espera en minutos al intentar establecer una conexión antes de terminar el intento.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

