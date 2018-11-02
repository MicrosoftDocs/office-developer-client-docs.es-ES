---
title: WillExecute (evento, ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4025645e5f8b12325ba20497ca6ef2b70175df
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919454"
---
# <a name="willexecute-event-ado"></a>WillExecute (evento, ADO)


**Se aplica a**: Access 2013, Office 2013


El evento **WillExecute** se utiliza (recibe una llamada) justo antes de que un comando pendiente se ejecute sobre una conexión.

## <a name="syntax"></a>Sintaxis

WillExecute*origen*, *CursorType*, *LockType*, *Opciones*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Parámetros

  - *Origen*

  - **String** que contiene un comando SQL o un nombre de procedimiento almacenado.

  - *CursorType*

  - Valor de tipo [CursorTypeEnum](cursortypeenum.md) que contiene el tipo de cursor para el objeto **Recordset** que se abrirá. Con este parámetro, puede cambiar el cursor a cualquier tipo durante una operación de [apertura](open-method-ado-recordset.md) del **objeto Recordset** . *CursorType* se omitirá para cualquier otra operación.

  - *LockType*

  - Valor de tipo [LockTypeEnum](locktypeenum.md) que contiene el tipo de bloqueo para el objeto **Recordset** que se abrirá. Con este parámetro, es posible cambiar el bloqueo a cualquier tipo durante una operación del método **Open** de un objeto **Recordset**. *LockType* se omitirá para cualquier otra operación.

  - *Options*

  - Valor de tipo **Long** que indica las opciones que se pueden usar para ejecutar el comando o abrir el objeto **Recordset**.

  - *valor de adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores, o en **adStatusCancel** para solicitar la cancelación de la operación que provocó el evento.

  - *pCommand*

  - Objeto [Command](command-object-ado.md) al que se aplica esta notificación de evento.

  - *Connection*

  - Objeto [Recordset](recordset-object-ado.md) al que se aplica esta notificación de evento.

  - *pConnection*

  - Objeto [Connection](connection-object-ado.md) al que se aplica esta notificación de evento.

## <a name="remarks"></a>Comentarios

Un evento **WillExecute** puede ocurrir debido a un **conexión.** [Ejecutar](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **comando.** [Ejecutar](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), o **Recordset.** Método [Open](open-method-ado-recordset.md) el parámetro *pConnection* siempre debe contener una referencia válida a un objeto **Connection** . Si el evento es debido a **Connection.Execute**, los parámetros *pRecordset* y *pCommand* se establecen en **Nothing**. Si el evento es debido a **un método Recordset.Open**, el parámetro *pRecordset* hará referencia al objeto de **conjunto de registros** y el parámetro *pCommand* se establece en **Nothing**. Si el evento es debido a **un método Command.Execute**, el parámetro *pCommand* hará referencia al objeto de **comando** y el parámetro *pRecordset* se establece en **Nothing**.

**WillExecute** permite examinar y modificar los parámetros pendientes de ejecución. Este evento puede devolver una petición para cancelar el comando pendiente.

