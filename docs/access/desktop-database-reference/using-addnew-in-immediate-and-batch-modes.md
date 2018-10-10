---
title: Utilizar AddNew en modos Inmediato y Proceso por lotes
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b37acc1819d12acc1e659be85361c3c09b84ebdb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484364"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a><span data-ttu-id="33bf7-102">Utilizar AddNew en modos Inmediato y Proceso por lotes</span><span class="sxs-lookup"><span data-stu-id="33bf7-102">Using AddNew in Immediate and Batch Modes</span></span>


<span data-ttu-id="33bf7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="33bf7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="33bf7-104">El comportamiento del método **AddNew** depende del modo de actualización del objeto **Recordset** y si se pasan los argumentos *FieldList* y *Values* .</span><span class="sxs-lookup"><span data-stu-id="33bf7-104">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *FieldList* and *Values* arguments.</span></span>

<span data-ttu-id="33bf7-p101">En modo de actualización inmediata (en el que el proveedor escribe los cambios en el origen de datos subyacente una vez que se ha llamado al método **Update**), si se llama al método **AddNew** sin argumentos, la propiedad **EditMode** se establece en **adEditAdd**. El proveedor almacena en caché localmente los cambios de valor de campo. Si se llama al método **Update**, se envía el nuevo registro a la base de datos y se restablece la propiedad **EditMode** en **adEditNone**. Si pasa los argumentos *FieldList* y *Values*, ADO envía inmediatamente el nuevo registro a la base de datos (sin necesidad de una llamada a **Update**); el valor de la propiedad **EditMode** no cambia (**adEditNone**).</span><span class="sxs-lookup"><span data-stu-id="33bf7-p101">In immediate update mode (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd.** The provider caches any field value changes locally. Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone**. If you pass the *FieldList* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="33bf7-109">En modo de actualización por lotes, si se llama al método **AddNew** sin argumentos, la propiedad **EditMode** se establece en **adEditAdd**.</span><span class="sxs-lookup"><span data-stu-id="33bf7-109">In batch update mode, calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="33bf7-110">El proveedor almacena en caché localmente los cambios de valor de campo.</span><span class="sxs-lookup"><span data-stu-id="33bf7-110">The provider caches any field value changes locally.</span></span> <span data-ttu-id="33bf7-111">Si se llama al método **Update**, el nuevo registro se agrega al **conjunto de registros** activo y la propiedad **EditMode** se restablece en **adEditNone**, pero el proveedor no envía los cambios a la base de datos subyacente hasta que se llame al método **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="33bf7-111">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="33bf7-112">Si se pasan los argumentos *FieldList* y *Values* , ADO envía el nuevo registro al proveedor para el almacenamiento en caché; debe llamar al método **UpdateBatch** para enviar el nuevo registro a la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="33bf7-112">If you pass the *FieldList* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span> <span data-ttu-id="33bf7-113">Para obtener más información acerca de **Update** y **UpdateBatch**, vea [Capítulo 5: Actualizar y almacenar datos.](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="33bf7-113">For more information about **Update** and **UpdateBatch**, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

