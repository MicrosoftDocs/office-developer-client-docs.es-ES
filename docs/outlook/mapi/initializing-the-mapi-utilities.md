---
title: Inicializar las herramientas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420951"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="e908d-103">Inicializar las herramientas MAPI</span><span class="sxs-lookup"><span data-stu-id="e908d-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="e908d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e908d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e908d-105">Si la única parte de MAPI que debe usar son las utilidades, las interfaces y las funciones declaradas en la MAPIUTIL de MAPI. H, como **IPropData** y **ITableData** , no es necesario llamar a **MAPIInitialize** para la inicialización.</span><span class="sxs-lookup"><span data-stu-id="e908d-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="e908d-106">Para obtener más información, vea [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)y [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="e908d-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="e908d-107">En su lugar, llame a la función **ScInitMapiUtil** .</span><span class="sxs-lookup"><span data-stu-id="e908d-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="e908d-108">Para obtener más información, vea [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="e908d-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="e908d-109">**ScInitMapiUtil** permite a las aplicaciones cliente utilizar funciones y métodos de utilidad que requieren asignadores MAPI, pero que no las solicitan explícitamente.</span><span class="sxs-lookup"><span data-stu-id="e908d-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="e908d-110">En el momento del cierre, haga una llamada a **DeinitMapiUtil** para liberar los recursos conectados a las utilidades.</span><span class="sxs-lookup"><span data-stu-id="e908d-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="e908d-111">No llame a **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="e908d-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="e908d-112">Para obtener más información, vea [DeinitMapiUtil](deinitmapiutil.md) y [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="e908d-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="e908d-113">Tenga en cuenta que la interfaz **ITableData** no admite notificaciones de tabla para clientes que hayan llamado a **ScInitMapiUtil** en lugar de **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="e908d-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

