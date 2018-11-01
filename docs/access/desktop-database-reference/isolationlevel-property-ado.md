---
title: IsolationLevel (propiedad, ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76978d33fc5f82c9b1f8137b64a663e7e95f2204
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883060"
---
# <a name="isolationlevel-property-ado"></a>IsolationLevel (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el nivel de aislamiento de un objeto [Connection](connection-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [IsolationLevelEnum](isolationlevelenum.md). El valor predeterminado es **adXactChaos**.

## <a name="remarks"></a>Comentarios

Use la propiedad **IsolationLevel** para establecer el nivel de aislamiento de un objeto **Connection**. El valor no se aplica hasta la siguiente vez que se llama al método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si el nivel de aislamiento solicitado no está disponible, el proveedor puede devolver el siguiente mayor valor de aislamiento.

La propiedad **IsolationLevel** es de lectura y escritura.

**Uso de servicio de datos remotos** Cuando se usa en un objeto Connection de cliente, se puede establecer la propiedad **IsolationLevel** sólo en **adXactUnspecified**.

Puesto que los usuarios están trabajando con objetos **Recordset** desconectados en una memoria caché del cliente, puede haber problemas de multiusuario. Por ejemplo, cuando dos usuarios diferentes intenten actualizar el mismo registro, el Servicio de datos remoto sólo permitirá que "gane" el usuario que actualice el registro en primer lugar. La solicitud de actualización del segundo usuario dará lugar a un error.

