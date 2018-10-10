---
title: Adición de registros (referencia de escritorio de la base de datos de Access)
TOCTitle: Adding Records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bfa1503e7f7b874136ab5aee70721a3b9cf3463b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486282"
---
# <a name="adding-records"></a><span data-ttu-id="b5e94-102">Agregar registros</span><span class="sxs-lookup"><span data-stu-id="b5e94-102">Adding Records</span></span>


<span data-ttu-id="b5e94-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5e94-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b5e94-p101">Utilice el método **AddNew** para crear e inicializar un registro nuevo en un **conjunto de registros** existente. Puede utilizar el método **Supports** con un valor **CursorOptionEnum** de **adAddNew** para comprobar si puede agregar registros al objeto **Recordset** activo.</span><span class="sxs-lookup"><span data-stu-id="b5e94-p101">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**. You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="b5e94-p102">Después de llamar al método **AddNew**, el registro nuevo pasa a ser el registro actual y sigue siéndolo después de llamar al método **Update**. Si el objeto **Recordset** no admite marcadores, tal vez no tenga acceso al registro nuevo cuando se haya movido a otro registro. Por lo tanto, dependiendo de su tipo de cursor, es posible que tenga que llamar al método **Requery** para poder tener acceso al registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="b5e94-p102">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method. If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record. Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="b5e94-109">Si llama a **AddNew** mientras modifica el registro actual o agrega un registro nuevo, ADO llamará al método **Update** para guardar todos los cambios y, después, ADO creará el registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="b5e94-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

