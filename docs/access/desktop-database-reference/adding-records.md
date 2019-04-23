---
title: Adición de registros (referencia de base de datos de escritorio de Access)
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 268cd381cdeef11f2a6f351160d930e4b169cfbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280290"
---
# <a name="adding-records"></a><span data-ttu-id="76427-102">Adición de registros</span><span class="sxs-lookup"><span data-stu-id="76427-102">Adding records</span></span>

<span data-ttu-id="76427-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76427-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76427-p101">Utilice el método **AddNew** para crear e inicializar un registro nuevo en un **conjunto de registros** existente. Puede utilizar el método **Supports** con un valor **CursorOptionEnum** de **adAddNew** para comprobar si puede agregar registros al objeto **Recordset** activo.</span><span class="sxs-lookup"><span data-stu-id="76427-p101">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**. You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="76427-p102">Después de llamar al método **AddNew**, el registro nuevo pasa a ser el registro actual y sigue siéndolo después de llamar al método **Update**. Si el objeto **Recordset** no admite marcadores, tal vez no tenga acceso al registro nuevo cuando se haya movido a otro registro. Por lo tanto, dependiendo de su tipo de cursor, es posible que tenga que llamar al método **Requery** para poder tener acceso al registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="76427-p102">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method. If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record. Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="76427-109">Si llama a **AddNew** mientras modifica el registro actual o agrega un registro nuevo, ADO llamará al método **Update** para guardar todos los cambios y, después, ADO creará el registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="76427-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="76427-110">Esta sección incluye los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="76427-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="76427-111">Adición de varios campos</span><span class="sxs-lookup"><span data-stu-id="76427-111">Adding multiple fields</span></span>](adding-multiple-fields.md)
- [<span data-ttu-id="76427-112">Determinación del modo de edición</span><span class="sxs-lookup"><span data-stu-id="76427-112">Determining Edit mode</span></span>](determining-edit-mode.md)
- [<span data-ttu-id="76427-113">Uso de AddNew en los modos inmediato y por lotes</span><span class="sxs-lookup"><span data-stu-id="76427-113">Using AddNew in Immediate and Batch modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

