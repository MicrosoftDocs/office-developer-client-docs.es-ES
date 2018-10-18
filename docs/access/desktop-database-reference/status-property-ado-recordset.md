---
title: Status (propiedad, Recordset ADO)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1979ad721a01ef72c08da1531a8826ec320915e5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604620"
---
# <a name="status-property-ado-recordset"></a>Status (propiedad, Recordset ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica el estado del registro actual con respecto a actualizaciones por lotes u otras operaciones masivas.

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve una suma de uno o más valores [RecordStatusEnum](recordstatusenum.md).

## <a name="remarks"></a>Comentarios

Use la propiedad **Status** para ver los cambios pendientes en los registros modificados durante la actualización por lotes. La propiedad **Status** también se puede usar para ver el estado de registros que producen error durante operaciones masivas, por ejemplo al llamar a los métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) o [CancelBatch](cancelbatch-method-ado.md) de un objeto [Recordset](recordset-object-ado.md) o al establecer la propiedad [Filter](filter-property-ado.md) de un objeto **Recordset** en una matriz de marcadores. Con esta propiedad, es posible determinar cómo se produjo el error de un registro determinado y solucionarlo en consecuencia.

