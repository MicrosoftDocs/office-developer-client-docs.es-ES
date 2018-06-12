---
title: Uso de las utilidades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 3f461d50e838aac0caee37d295ba8e86b9559bd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820961"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="d2a4e-103">Uso de las utilidades MAPI</span><span class="sxs-lookup"><span data-stu-id="d2a4e-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="d2a4e-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2a4e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2a4e-105">Las utilidades MAPI se componen de datos de la tabla y objetos de datos de propiedad y una gran variedad de funciones para admitir las características varias.</span><span class="sxs-lookup"><span data-stu-id="d2a4e-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="d2a4e-106">Es posible que un cliente necesita sólo estas utilidades y no tiene que iniciar sesión en el subsistema MAPI para establecer una conexión con los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="d2a4e-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="d2a4e-107">Si el cliente se ajusta en esta categoría, llame a la función API [ScInitMapiUtil](scinitmapiutil.md) en lugar de la función [MAPIInitialize](mapiinitialize.md) en tiempo de inicialización.</span><span class="sxs-lookup"><span data-stu-id="d2a4e-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="d2a4e-108">**ScInitMapiUtil** permite a los clientes usar las funciones de utilidad que requieren asignadores de MAPI, pero que no le solicita a los asignadores de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="d2a4e-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="d2a4e-109">Cuando es el momento de apagar, llame a [DeinitMapiUtil](deinitmapiutil.md) para liberar recursos en lugar de [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="d2a4e-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="d2a4e-110">Los clientes que no llaman nunca **MAPIInitialize** no deben llamar a **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="d2a4e-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="d2a4e-111">Si se ha llamado **ScInitMapiUtil** en lugar de **MAPIInitialize** y usan tablas a través de los métodos de **ITableData** en lugar de a través de los métodos **IMAPITable** , tenga en cuenta que no funcionarán las notificaciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="d2a4e-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="d2a4e-112">Las notificaciones requieren el uso de las bibliotecas de MAPI y [IMAPITable: IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d2a4e-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

