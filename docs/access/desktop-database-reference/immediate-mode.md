---
title: Modo inmediato (referencia de escritorio de la base de datos de Access)
TOCTitle: Immediate mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abc2e8365c60987fedc0d306b274df74c7ee551
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706950"
---
# <a name="immediate-mode"></a>Modo Inmediato


**Se aplica a**: Access 2013, Office 2013

El modo inmediato está activo cuando la propiedad **LockType** se ha establecido en **adLockOptimistic** o **adLockPessimistic**. En modo inmediato, los cambios en un registro se propagan al origen de datos en cuanto se declara completo el trabajo en una fila llamando al método **Update**.

## <a name="calling-update"></a>Llamar a Update

Si se mueve del registro que está agregando o editando antes de llamar al método **Update**, ADO llama automáticamente a **Update** para guardar los cambios. Debe llamar al método **CancelUpdate** antes de desplazarse si desea cancelar los cambios realizados en el registro activo o descartar un registro recién agregado.

El registro activo lo sigue estando después de llamar al método **Update**.

## <a name="cancelupdate"></a>CancelUpdate

Utilice el método **CancelUpdate** para cancelar los cambios realizados en la fila activa o descartar una fila recién agregada. Después de llamar al método **Update**, no se pueden cancelar los cambios en la fila activa o en una nueva fila a menos que dichos cambios sean parte de una transacción que se pueda deshacer con el método **RollbackTrans** o parte de una actualización por lotes. En el caso de una actualización por lotes, puede cancelar la **actualización** con el método **CancelUpdate** o **CancelBatch**.

Si va a agregar una fila nueva cuando llame al método **CancelUpdate**, la fila activa pasará a ser la fila que estaba activa antes de la llamada a **AddNew**.

Si no ha modificado la fila activa o si no ha agregado ninguna fila nueva, la llamada al método **CancelUpdate** genera un error.

