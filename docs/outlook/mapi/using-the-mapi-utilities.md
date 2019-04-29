---
title: Uso de las herramientas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409989"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="a33cc-103">Uso de las herramientas MAPI</span><span class="sxs-lookup"><span data-stu-id="a33cc-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="a33cc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a33cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a33cc-105">Las utilidades MAPI se componen de datos de tabla y objetos de datos de propiedad, y una variedad de funciones para admitir varias características.</span><span class="sxs-lookup"><span data-stu-id="a33cc-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="a33cc-106">Es posible que un cliente solo necesite estas herramientas y que no tenga que iniciar sesión en el subsistema MAPI para establecer una conexión con los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="a33cc-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="a33cc-107">Si el cliente encaja en esta categoría, llame a la función de la API [ScInitMapiUtil](scinitmapiutil.md) en lugar de la función [MAPIInitialize](mapiinitialize.md) en el momento de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="a33cc-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="a33cc-108">**ScInitMapiUtil** permite a los clientes usar funciones de utilidad que requieren asignadores MAPI, pero que no solicitan los asignadores de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="a33cc-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="a33cc-109">Cuando sea el momento de apagar, llame a [DeinitMapiUtil](deinitmapiutil.md) para liberar recursos en lugar de [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="a33cc-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="a33cc-110">Los clientes que nunca llaman a **MAPIInitialize** no deben llamar a **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="a33cc-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="a33cc-111">Si ha llamado **ScInitMapiUtil** en lugar de **MAPIInitialize** y está usando tablas a través de los métodos de **ITableData** en lugar de los métodos **IMAPITable** , tenga en cuenta que las notificaciones de tabla no funcionarán.</span><span class="sxs-lookup"><span data-stu-id="a33cc-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="a33cc-112">Las notificaciones requieren el uso de las bibliotecas MAPI y el [IMAPITable: IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a33cc-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

