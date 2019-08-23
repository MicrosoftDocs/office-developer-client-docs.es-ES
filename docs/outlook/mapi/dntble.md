---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Última modificación: 05 de julio de 2012'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337117"
---
# <a name="dntble"></a><span data-ttu-id="d4d50-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="d4d50-103">DNTBLE</span></span>

  
  
<span data-ttu-id="d4d50-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4d50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4d50-105">Información para descargar el contenido de una carpeta del servidor durante el [estado descargar tabla](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="d4d50-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="d4d50-106">Este proceso de descarga usa la sincronización de cambio incremental (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="d4d50-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="d4d50-107">Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d4d50-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d4d50-108">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d4d50-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="d4d50-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d4d50-109">Members</span></span>

 <span data-ttu-id="d4d50-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="d4d50-110">_cEntNew_</span></span>
  
> <span data-ttu-id="d4d50-111">[salida] Número de elementos añadidos al almacén local.</span><span class="sxs-lookup"><span data-stu-id="d4d50-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="d4d50-112">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="d4d50-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="d4d50-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="d4d50-113">_cEntMod_</span></span>
  
> <span data-ttu-id="d4d50-114">[salida] Número de elementos modificados en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="d4d50-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="d4d50-115">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="d4d50-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="d4d50-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="d4d50-116">_cEntRead_</span></span>
  
> <span data-ttu-id="d4d50-117">[salida] Número de elementos leídos o marcados como no leídos en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="d4d50-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="d4d50-118">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="d4d50-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="d4d50-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="d4d50-119">_cEntDel_</span></span>
  
> <span data-ttu-id="d4d50-120">[salida] Número de elementos eliminados en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="d4d50-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="d4d50-121">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="d4d50-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4d50-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4d50-122">See also</span></span>



[<span data-ttu-id="d4d50-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="d4d50-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d4d50-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d4d50-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d4d50-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="d4d50-125">DNTBL</span></span>](dntbl.md)

