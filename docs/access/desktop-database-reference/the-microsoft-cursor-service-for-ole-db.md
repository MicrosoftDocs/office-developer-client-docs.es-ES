---
title: El servicio de cursores de Microsoft para OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce8ebea2e9ce1f31adc239195614f4a8b1e2bd1b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722623"
---
# <a name="microsoft-cursor-service-for-ole-db"></a><span data-ttu-id="70bab-102">Servicio de cursores de Microsoft para OLE DB</span><span class="sxs-lookup"><span data-stu-id="70bab-102">Microsoft Cursor Service for OLE DB</span></span>


<span data-ttu-id="70bab-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70bab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70bab-p101">Cuando selecciona un cursor en el cliente o establece la propiedad **CursorLocation** en **adUseClient**, está invocando el servicio de cursores de Microsoft para OLE DB. También puede ver referencias a "Client Cursor Engine" (Motor de cursores clientes) que, en esencia, es lo mismo en el contexto de ADO. Este servicio complementa las funciones de soporte de cursores de los proveedores de datos. En consecuencia, se puede percibir una funcionalidad relativamente uniforme de todos los proveedores de datos.</span><span class="sxs-lookup"><span data-stu-id="70bab-p101">When you select a client-side cursor, or set the **CursorLocation** property to **adUseClient**, you are invoking the Microsoft Cursor Service for OLE DB. You might also see references to the "Client Cursor Engine", which is essentially the same thing in the context of ADO. This service supplements the cursor-support functions of data providers. As a result, you can perceive relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="70bab-p102">Con el servicio de cursor para OLE DB, las propiedades dinámicas están disponibles y el comportamiento de ciertos métodos mejora. Por ejemplo, la propiedad dinámica **Optimizar** habilita a la creación de índices temporales para facilitar determinadas operaciones, como el método **Find**.</span><span class="sxs-lookup"><span data-stu-id="70bab-p102">The Cursor Service for OLE DB makes dynamic properties available and enhances the behavior of certain methods. For example, the **Optimize** dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the **Find** method.</span></span>

<span data-ttu-id="70bab-p103">El servicio de cursor habilita la compatibilidad con la actualización por lotes en todos los casos. También simula tipos de cursor más capaces, como los cursores dinámicos, cuando un proveedor de datos sólo puede suministrar cursores menos capaces, como cursores estáticos.</span><span class="sxs-lookup"><span data-stu-id="70bab-p103">The Cursor Service enables support for batch updating in all cases. It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

