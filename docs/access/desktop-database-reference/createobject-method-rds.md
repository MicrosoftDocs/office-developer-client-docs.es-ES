---
title: Método CreateObject (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ad61495bcc96b3099af6273796626e9442cbf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295376"
---
# <a name="createobject-method-rds"></a>Método CreateObject (RDS)

**Se aplica a:** Access 2013, Office 2013

Crea el proxy para el objeto de negocio de destino y devuelve un puntero al mismo. El proxy empaqueta y calcula las referencias de los datos en el código auxiliar de servidor para permitir la comunicación con el objeto de negocio y enviar solicitudes y datos a través de Internet. Para los objetos componentes en proceso, no se utiliza ningún proxy; solo se proporciona un puntero al objeto.

## <a name="syntax"></a>Sintaxis

El Servicio de datos remotos (RDS) admite los protocolos siguientes: HTTP, HTTPS (HTTP a través de Capa de sockets seguros), DCOM y en proceso.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Protocolo</p></th>
<th><p>Sintaxis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>HTTP</p></td>
<td><p>Establecer<em>el objeto</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p>Establecer<em>el objeto</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p>Establecer<em>el objeto</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>computername</em> &quot; )</p></td>
</tr>
<tr class="even">
<td><p>Dentro del proceso</p></td>
<td><p>Establecer<em>el objeto</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; &quot; )</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Objeto* |Variable de objeto que da como resultado un objeto que es el tipo especificado en *ProgID*.|
|*DataSpace* |Variable de objeto que representa un objeto [RDS.DataSpace](dataspace-object-rds.md) utilizado para crear una instancia del objeto nuevo.|
|*ProgID* |Valor de tipo **String** que contiene el identificador de programación que especifica un objeto de negocio de servidor que implementa las reglas de negocios de la aplicación.|
|*awebsrvr* o *computername* |Valor de tipo **String** que representa una dirección URL que identifica el servidor web de Internet Information Services (IIS) donde se crea una instancia del objeto de negocio del servidor.|

## <a name="remarks"></a>Comentarios

El *protocolo HTTP* es el protocolo web estándar; *HTTPS* es un protocolo web seguro. Utilice el *protocolo DCOM* cuando ejecute una red de área local sin HTTP. El protocolo *en proceso* es una biblioteca de vínculos dinámicos (DLL) local; no utiliza una red.

