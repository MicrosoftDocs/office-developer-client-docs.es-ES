---
title: CursorLocation (propiedad, ADO)
TOCTitle: CursorLocation Property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9805b032a0e1a203d2a4057fb74757826a2a47b4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485129"
---
# <a name="cursorlocation-property-ado"></a>CursorLocation (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica la ubicación del servicio de cursores.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long** que puede establecerse en uno de los valores de [CursorLocationEnum](cursorlocationenum.md).

## <a name="remarks"></a>Comentarios

Esta propiedad permite elegir entre varias bibliotecas de cursores accesibles para el proveedor. Normalmente, se puede elegir entre una biblioteca de cursores de cliente y otra ubicada en el servidor.

El valor de esta propiedad afecta sólo a las conexiones establecidas después de la configuración de la propiedad. Si se modifica la propiedad **CursorLocation**, no se verán afectadas las conexiones existentes.

Los cursores devueltos por el método [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) heredan este valor de configuración. Los objetos **Recordset** heredarán automáticamente este valor de sus conexiones asociadas.

Esta propiedad es de lectura y escritura en un objeto [Connection](connection-object-ado.md) o un objeto [Recordset](recordset-object-ado.md) cerrado, y es de sólo lectura en un objeto **Recordset** abierto.

**Uso de servicio de datos remotos** Cuando se usa en un objeto de **conexión** o un **conjunto de registros** del lado cliente, sólo puede establecerse la propiedad **CursorLocation** en **adUseClient**.

