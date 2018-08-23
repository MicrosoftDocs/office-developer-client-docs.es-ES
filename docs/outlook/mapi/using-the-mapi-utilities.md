---
title: Usar las herramientas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4612b6f345d59d988013671758c6d0579aaa127d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569536"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="51c2d-103">Usar las herramientas MAPI</span><span class="sxs-lookup"><span data-stu-id="51c2d-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="51c2d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51c2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51c2d-105">Las utilidades MAPI se componen de datos de la tabla y objetos de datos de propiedad y una gran variedad de funciones para admitir las características varias.</span><span class="sxs-lookup"><span data-stu-id="51c2d-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="51c2d-106">Es posible que un cliente necesita sólo estas utilidades y no tiene que iniciar sesión en el subsistema MAPI para establecer una conexión con los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="51c2d-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="51c2d-107">Si el cliente se ajusta en esta categoría, llame a la función API [ScInitMapiUtil](scinitmapiutil.md) en lugar de la función [MAPIInitialize](mapiinitialize.md) en tiempo de inicialización.</span><span class="sxs-lookup"><span data-stu-id="51c2d-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="51c2d-108">**ScInitMapiUtil** permite a los clientes usar las funciones de utilidad que requieren asignadores de MAPI, pero que no le solicita a los asignadores de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="51c2d-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="51c2d-109">Cuando es el momento de apagar, llame a [DeinitMapiUtil](deinitmapiutil.md) para liberar recursos en lugar de [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="51c2d-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="51c2d-110">Los clientes que no llaman nunca **MAPIInitialize** no deben llamar a **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="51c2d-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="51c2d-111">Si se ha llamado **ScInitMapiUtil** en lugar de **MAPIInitialize** y usan tablas a través de los métodos de **ITableData** en lugar de a través de los métodos **IMAPITable** , tenga en cuenta que no funcionarán las notificaciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="51c2d-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="51c2d-112">Las notificaciones requieren el uso de las bibliotecas de MAPI y [IMAPITable: IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="51c2d-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

