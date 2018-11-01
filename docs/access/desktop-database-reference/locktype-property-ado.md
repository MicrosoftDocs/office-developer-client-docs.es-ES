---
title: LockType (propiedad, ADO)
TOCTitle: LockType property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88657361d6ce5ac168f21f5709bdaf68eeb23b6d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879063"
---
# <a name="locktype-property-ado"></a><span data-ttu-id="b948d-102">LockType (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="b948d-102">LockType property (ADO)</span></span>


<span data-ttu-id="b948d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b948d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b948d-104">Indica el tipo de bloqueos colocados en registros durante la modificación.</span><span class="sxs-lookup"><span data-stu-id="b948d-104">Indicates the type of locks placed on records during editing.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b948d-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b948d-105">Settings and return values</span></span>

<span data-ttu-id="b948d-p101">Establece o devuelve un valor de tipo [LockTypeEnum](locktypeenum.md). El valor predeterminado es **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="b948d-p101">Sets or returns a [LockTypeEnum](locktypeenum.md) value. The default value is **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b948d-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b948d-108">Remarks</span></span>

<span data-ttu-id="b948d-p102">Establezca la propiedad **LockType** antes de abrir un objeto [Recordset](recordset-object-ado.md) a fin de especificar el tipo de bloqueo que el proveedor debe usar al abrirlo. Lea la propiedad para devolver el tipo de bloqueo en uso a un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b948d-p102">Set the **LockType** property before opening a [Recordset](recordset-object-ado.md) to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="b948d-p103">Es posible que los proveedores no admitan todos los tipos de bloqueo. Si un proveedor no puede admitir el valor **LockType** solicitado, lo sustituirá por otro tipo de bloqueo. Para determinar la funcionalidad de bloqueo real disponible en un objeto **Recordset**, use el método [Supports](supports-method-ado.md) con **adUpdate** y **adUpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="b948d-p103">Providers may not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="b948d-p104">No se admite el valor **adLockPessimistic** cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**. Si se establece un valor no admitido, no se producirá ningún error; se utilizará el valor admitido de **LockType** más cercano.</span><span class="sxs-lookup"><span data-stu-id="b948d-p104">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="b948d-116">La propiedad **LockType** es de lectura y escritura cuando el objeto **Recordset** está cerrado y de sólo lectura cuando está abierto.</span><span class="sxs-lookup"><span data-stu-id="b948d-116">The **LockType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="b948d-117">**Uso de servicio de datos remotos** Cuando se usa en un objeto Recordset de cliente, sólo puede establecerse la propiedad **LockType** en **adLockBatchOptimistic**.</span><span class="sxs-lookup"><span data-stu-id="b948d-117">**Remote Data Service Usage**When used on a client-side Recordset object, the **LockType** property can only be set to **adLockBatchOptimistic**.</span></span>

