---
title: Modo inmediato (referencia de escritorio de la base de datos de Access)
TOCTitle: Immediate Mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9448844afa167af3e34e609145ba50d549a9930a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884908"
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

