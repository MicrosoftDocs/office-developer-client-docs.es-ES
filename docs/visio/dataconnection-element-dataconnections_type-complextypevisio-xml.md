---
title: Elemento DataConnection (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Abstrae la comunicación entre uno o varios elementos DataRecordset y un origen de datos que no es XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538406"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a>Elemento DataConnection (DataConnections_Type complexType) (Visio XML)

Abstrae la comunicación entre uno o varios **elementos DataRecordset** y un origen de datos que no es XML. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |connections.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Contiene los **elementos DataConnection** del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |opcional  <br/> |El valor predeterminado es False. Para obtener más información, vea los Comentarios.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|Comando  <br/> |xsd:string  <br/> |opcional  <br/> |Cadena de comandos usada para consultar el origen de datos.  <br/> |Valores del tipo xsd:string.  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |opcional  <br/> |La cadena de conexión que define los parámetros necesarios para conectarse a un origen de datos.  <br/> |Valores del tipo xsd:string.  <br/> |
|FileName  <br/> |xsd:string  <br/> |necesario  <br/> |Nombre del archivo de conexión. Para obtener más información, vea los Comentarios.  <br/> |Valores del tipo xsd:string.  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |opcional  <br/> |Un usuario proporcionó el nombre para la conexión de datos.  <br/> |Valores del tipo xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El identificador asignado por Visio para una conexión determinada, única en el documento.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Tiempo de espera en minutos al intentar establecer una conexión antes de finalizar el intento.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

