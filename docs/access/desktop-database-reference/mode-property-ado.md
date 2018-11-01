---
title: Mode (propiedad, ADO)
TOCTitle: Mode property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 74b0a401c5fbd7e34cbd002020d81b9b0858e4f7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874282"
---
# <a name="mode-property-ado"></a>Mode (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica los permisos disponibles para modificar datos de un objeto [Connection](connection-object-ado.md), [Record](record-object-ado.md) o [Stream](stream-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [ConnectModeEnum](connectmodeenum.md). El valor predeterminado de **Connection** es **adModeUnknown**, el de **Record** es **adModeRead** y el de un objeto **Stream** asociado a un origen subyacente (abierto con una dirección URL como origen o como el objeto **Stream** predeterminado de **Record**) es **adModeRead**. El valor predeterminado de un objeto **Stream** no asociado a un origen subyacente (con una instancia en memoria) es **adModeUnknown**.

## <a name="remarks"></a>Comentarios

Use la propiedad **Mode** para establecer o devolver los permisos de acceso utilizados por el proveedor en la conexión actual. La propiedad **Mode** solo se puede establecer cuando el objeto **Connection** está cerrado.

En un objeto **Stream**, si no se ha especificado el modo de acceso, se hereda del origen utilizado para abrir el objeto **Stream**. Por ejemplo, si se abre un objeto **Stream** desde un objeto **Record**, se abre de forma predeterminada del mismo modo que el objeto **Record**.

Esta propiedad es de lectura y escritura mientras el objeto está cerrado y de sólo lectura mientras está abierto.

**Uso de servicio de datos remotos** Cuando se usa en un objeto Connection de cliente, la propiedad **Mode** sólo puede establecerse en el **valor adModeUnknown**.

