---
title: Evento WillExecute (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe15604d0160afcbde5fdf02eaa6a7831da874b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302761"
---
# <a name="willexecute-event-ado"></a>Evento WillExecute (ADO)

**Se aplica a:** Access 2013, Office 2013

El evento **WillExecute** se utiliza (recibe una llamada) justo antes de que un comando pendiente se ejecute sobre una conexión.

## <a name="syntax"></a>Sintaxis

WillExecute *Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Source* |**String** que contiene un comando SQL o un nombre de procedimiento almacenado.|
|*CursorType* |Valor de tipo [CursorTypeEnum](cursortypeenum.md) que contiene el tipo de cursor para el objeto **Recordset** que se abrirá. Con este parámetro, puede cambiar el cursor a cualquier tipo durante una **operación Recordset** [Open.](open-method-ado-recordset.md) *CursorType* se omitirá para cualquier otra operación.|
|*LockType* |Valor de tipo [LockTypeEnum](locktypeenum.md) que contiene el tipo de bloqueo para el objeto **Recordset** que se abrirá. Con este parámetro, es posible cambiar el bloqueo a cualquier tipo durante una operación del método **Open** de un objeto **Recordset**. *LockType* se omitirá para cualquier otra operación.|
|*Options* |Valor de tipo **Long** que indica las opciones que se pueden usar para ejecutar el comando o abrir el objeto **Recordset**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores, o en **adStatusCancel** para solicitar la cancelación de la operación que provocó el evento.|
|*pCommand* |Objeto [Command](command-object-ado.md) al que se aplica esta notificación de evento.|
|*pRecordset* |Objeto [Recordset](recordset-object-ado.md) al que se aplica esta notificación de evento.|
|*pConnection* |Objeto [Connection](connection-object-ado.md) al que se aplica esta notificación de evento.|

## <a name="remarks"></a>Comentarios

Un evento **WillExecute** puede ocurrir debido a un método **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) o **Recordset.**[Open](open-method-ado-recordset.md). El parámetro *pConnection* debería contener siempre una referencia válida a un objeto **Connection**. Si el evento es debido a un método **Connection.Execute**, los parámetros *pRecordset* y *pCommand* se establecen en **Nothing**. Si el evento se debe a un método **Recordset.Open**, el parámetro *pRecordset* hará referencia al objeto **Recordset**, mientras que el parámetro *pCommand* se establecerá en **Nothing**. Si el evento se debe a un método **Command.Execute**, el parámetro *pCommand* hará referencia al objeto **Command**, mientras que el parámetro *pRecordset* se establecerá en **Nothing**.

**WillExecute** permite examinar y modificar los parámetros pendientes de ejecución. Este evento puede devolver una petición para cancelar el comando pendiente.

