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
ms.openlocfilehash: 8ee0504d4a8b9e2ce96e42a53b778d4e3f518fcc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817818"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="7b508-103">Inicializar las herramientas MAPI</span><span class="sxs-lookup"><span data-stu-id="7b508-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="7b508-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b508-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b508-105">Si la única parte de MAPI que necesita para usar son las utilidades, las interfaces y funciones declaran en MAPIUTIL de MAPI. Archivo de encabezado según se trate como **IPropData** y **ITableData** : no es necesario llamar a **MAPIInitialize** para la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7b508-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="7b508-106">Para obtener más información, vea [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)y [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="7b508-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="7b508-107">En su lugar, llame a la función **ScInitMapiUtil** .</span><span class="sxs-lookup"><span data-stu-id="7b508-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="7b508-108">Para obtener más información, vea [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="7b508-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="7b508-109">**ScInitMapiUtil** permite que las aplicaciones de cliente usar las funciones de utilidad y métodos que requieren asignadores de MAPI, pero que no los pida explícitamente.</span><span class="sxs-lookup"><span data-stu-id="7b508-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="7b508-110">Durante el apagado, realice una llamada a **DeinitMapiUtil** para liberar recursos conectados a las utilidades.</span><span class="sxs-lookup"><span data-stu-id="7b508-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="7b508-111">No llame a **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="7b508-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="7b508-112">Para obtener más información, vea [DeinitMapiUtil](deinitmapiutil.md) y [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="7b508-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="7b508-113">Tenga en cuenta que la interfaz de **ITableData** no admite las notificaciones de tabla para los clientes que se han llamado **ScInitMapiUtil** en lugar de **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="7b508-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  
