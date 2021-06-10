---
title: ¿Qué es un bloqueo? (Referencia de base de datos de escritorio de Access)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e503fd15d9864cc6ab007de031493e321622246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306765"
---
# <a name="what-is-a-lock"></a><span data-ttu-id="1f6db-103">¿Qué es un bloqueo?</span><span class="sxs-lookup"><span data-stu-id="1f6db-103">What is a lock?</span></span>


<span data-ttu-id="1f6db-104">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f6db-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f6db-p102">El bloqueo es el proceso mediante el cual un sistema de administración de bases de datos (DBMS) restringe el acceso a una fila en un entorno multiusuario. Cuando una fila o una columna se bloquean de forma exclusiva, el acceso a los datos bloqueados queda cerrado mientras no se libere el bloqueo. De este modo, se garantiza que dos usuarios no puedan actualizar simultáneamente la misma columna de una fila.</span><span class="sxs-lookup"><span data-stu-id="1f6db-p102">Locking is the process by which a DBMS restricts access to a row in a multi-user environment. When a row or column is exclusively locked, other users are not permitted to access the locked data until the lock is released. This ensures that two users cannot simultaneously update the same column in a row.</span></span>

<span data-ttu-id="1f6db-p103">Los bloqueos pueden ser muy costosos en cuanto a recursos y, por tanto, sólo se deben utilizar cuando sea necesario para preservar la integridad de los datos. En una base de datos en la que cientos o miles de usuarios podrían estar intentando obtener acceso a un registro cada segundo (por ejemplo, una base de datos en Internet), el uso de bloqueos innecesarios podría reducir el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1f6db-p103">Locks can be very expensive from a resource perspective and should be used only when required to preserve data integrity. In a database where hundreds or thousands of users could be trying to access a record every second — such as a database connected to the Internet — unnecessary locking could quickly result in slower performance in your application.</span></span>

<span data-ttu-id="1f6db-110">La forma en que el origen de datos y la biblioteca de cursores ADO supervisan la concurrencia se puede controlar si elige la opción de bloqueo apropiada.</span><span class="sxs-lookup"><span data-stu-id="1f6db-110">You can control how the data source and the ADO cursor library manage concurrency by choosing the appropriate locking option.</span></span>

<span data-ttu-id="1f6db-p104">Establezca la propiedad **LockType** antes de abrir un objeto **Recordset** para especificar qué tipo de bloqueo debe usar el proveedor al abrirlo. Lea la propiedad para obtener el tipo de bloqueo usado en un objeto **Recordset** abierto de este tipo.</span><span class="sxs-lookup"><span data-stu-id="1f6db-p104">Set the **LockType** property before opening a **Recordset** to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="1f6db-p105">Puede que los proveedores no admitan todos los tipos de bloqueo. Si un proveedor no admite la opción **LockType** solicitada, la sustituirá por otro tipo de bloqueo. Utilice el método **Supports** con [adUpdate](supports-method-ado.md) y **adUpdateBatch** para determinar la funcionalidad real de bloqueo disponible en un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1f6db-p105">Providers might not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="1f6db-p106">El valor **adLockPessimistic** no se admite si la propiedad [CursorLocation](cursorlocation-property-ado.md) se establece en **adUseClient**. Si se establece un valor no admitido, no se producirá ningún error; en su lugar, se utilizará el **LockType** admitido más próximo.</span><span class="sxs-lookup"><span data-stu-id="1f6db-p106">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="1f6db-118">La propiedad **LockType** es de lectura y escritura cuando el objeto **Recordset** está cerrado, y de solo lectura cuando está abierto.</span><span class="sxs-lookup"><span data-stu-id="1f6db-118">The **LockType** property is read/write when the **Recordset** is closed, and read-only when it is open.</span></span>

<span data-ttu-id="1f6db-119">En esta sección se incluye el siguiente tema:</span><span class="sxs-lookup"><span data-stu-id="1f6db-119">This section includes the following topic:</span></span>

- [<span data-ttu-id="1f6db-120">Tipos de bloqueos</span><span class="sxs-lookup"><span data-stu-id="1f6db-120">Types of Locks</span></span>](types-of-locks.md)

