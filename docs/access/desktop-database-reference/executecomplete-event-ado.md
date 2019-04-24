---
title: ExecuteComplete (evento, ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a094968e70ace5e6cba1df184bf0ba57c2d7789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293227"
---
# <a name="executecomplete-event-ado"></a>ExecuteComplete (evento, ADO)

**Se aplica a:** Access 2013, Office 2013

Al evento **ExecuteComplete** se le llama después de que un comando haya terminado de ejecutarse.

## <a name="syntax"></a>Sintaxis

ExecuteComplete*RecordsAffected*, *perror*, ** adStatus, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*RecordsAffected* |Valor **Long** que indica el número de registros afectados por el comando.|
|*pError* |Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de **adStatus** es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Antes de que este evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.|
|*pRecordset* |Objeto [Command](command-object-ado.md) que se ejecutó. Contiene un objeto **Command** incluso al llamar a **Connection.Execute** o a **Recordset.Open** sin crear explícitamente un objeto **Command**; en tales casos, ADO crea internamente el objeto **Command**.|
|*pRecordset* |Objeto [Recordset](recordset-object-ado.md) resultado del comando ejecutado. Este **Recordset** puede estar vacío. No debería nunca destruir este objeto Recordset desde dentro de este controlador de evento. Si lo hace, se producirá una infracción de acceso cuando ADO intente obtener acceso a un objeto que ya no existe.|
|*pConnection* |Objeto [Connection](connection-object-ado.md). La conexión sobre la que se ejecutó la operación.|

## <a name="remarks"></a>Comentarios

Un evento **ExecuteComplete** puede ocurrir debido a los métodos **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) o **Recordset.**[NextRecordset](nextrecordset-method-ado.md).

