---
title: ¿Qué es un bloqueo? (Referencia de escritorio de la base de datos de access)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48ecb0ca75a7cd8094e55fd82d153b2d941ceeeb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886126"
---
# <a name="what-is-a-lock"></a>¿Qué es un bloqueo?


**Se aplica a**: Access 2013, Office 2013

El bloqueo es el proceso mediante el cual un sistema de administración de bases de datos (DBMS) restringe el acceso a una fila en un entorno multiusuario. Cuando una fila o una columna se bloquean de forma exclusiva, el acceso a los datos bloqueados queda cerrado mientras no se libere el bloqueo. De este modo, se garantiza que dos usuarios no puedan actualizar simultáneamente la misma columna de una fila.

Los bloqueos pueden ser muy costosos en cuanto a recursos y, por tanto, sólo se deben utilizar cuando sea necesario para preservar la integridad de los datos. En una base de datos en la que cientos o miles de usuarios podrían estar intentando obtener acceso a un registro cada segundo (por ejemplo, una base de datos en Internet), el uso de bloqueos innecesarios podría reducir el rendimiento de la aplicación.

La forma en que el origen de datos y la biblioteca de cursores ADO supervisan la concurrencia se puede controlar si elige la opción de bloqueo apropiada.

Establezca la propiedad **LockType** antes de abrir un objeto **Recordset** para especificar qué tipo de bloqueo debe usar el proveedor al abrirlo. Lea la propiedad para obtener el tipo de bloqueo usado en un objeto **Recordset** abierto de este tipo.

Puede que los proveedores no admitan todos los tipos de bloqueo. Si un proveedor no admite la opción **LockType** solicitada, la sustituirá por otro tipo de bloqueo. Utilice el método **Supports** con [adUpdate](supports-method-ado.md) y **adUpdateBatch** para determinar la funcionalidad real de bloqueo disponible en un objeto **Recordset**.

El valor **adLockPessimistic** no se admite si la propiedad [CursorLocation](cursorlocation-property-ado.md) se establece en **adUseClient**. Si se establece un valor no admitido, no se producirá ningún error; en su lugar, se utilizará el **LockType** admitido más próximo.

La propiedad **LockType** es de lectura y escritura cuando el objeto **Recordset** está cerrado, y de solo lectura cuando está abierto.

En esta sección se incluye el siguiente tema:

- [Tipos de bloqueos](types-of-locks.md)

