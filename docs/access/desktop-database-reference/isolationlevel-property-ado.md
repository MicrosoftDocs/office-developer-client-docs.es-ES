---
title: Propiedad IsolationLevel (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4eb46fa97b831030617916d03557b5bf9af9606d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291152"
---
# <a name="isolationlevel-property-ado"></a>Propiedad IsolationLevel (ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el nivel de aislamiento de un objeto [Connection](connection-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [IsolationLevelEnum](isolationlevelenum.md). El valor predeterminado es **adXactChaos**.

## <a name="remarks"></a>Comentarios

Use la propiedad **IsolationLevel** para establecer el nivel de aislamiento de un objeto **Connection**. El valor no se aplica hasta la siguiente vez que se llama al método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si el nivel de aislamiento solicitado no está disponible, el proveedor puede devolver el siguiente mayor valor de aislamiento.

La propiedad **IsolationLevel** es de lectura y escritura.

**Uso del servicio de datos remotos** Cuando se usa en un objeto Connection del lado cliente, la propiedad **IsolationLevel** sólo se puede establecer en **adXactUnspecified**.

Puesto que los usuarios están trabajando con objetos **Recordset** desconectados en una memoria caché del cliente, puede haber problemas de multiusuario. Por ejemplo, cuando dos usuarios diferentes intenten actualizar el mismo registro, el Servicio de datos remoto sólo permitirá que "gane" el usuario que actualice el registro en primer lugar. La solicitud de actualización del segundo usuario dará lugar a un error.

