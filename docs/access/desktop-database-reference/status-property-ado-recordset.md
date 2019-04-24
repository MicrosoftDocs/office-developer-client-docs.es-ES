---
title: Status (propiedad, Recordset de ADO)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4017ff216c17479a69d6d07d0abe51b30fd5e680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308522"
---
# <a name="status-property-ado-recordset"></a>Status (propiedad, Recordset de ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el estado del registro actual con respecto a actualizaciones por lotes u otras operaciones masivas.

## <a name="return-value"></a>Valor devuelto

Devuelve una suma de uno o más valores [RecordStatusEnum](recordstatusenum.md).

## <a name="remarks"></a>Comentarios

Use la propiedad **Status** para ver los cambios pendientes en los registros modificados durante la actualización por lotes. La propiedad **Status** también se puede usar para ver el estado de registros que producen error durante operaciones masivas, por ejemplo al llamar a los métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) o [CancelBatch](cancelbatch-method-ado.md) de un objeto [Recordset](recordset-object-ado.md) o al establecer la propiedad [Filter](filter-property-ado.md) de un objeto **Recordset** en una matriz de marcadores. Con esta propiedad, es posible determinar cómo se produjo el error de un registro determinado y solucionarlo en consecuencia.

