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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391951"
---
# <a name="dntble"></a><span data-ttu-id="b6d9b-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="b6d9b-103">DNTBLE</span></span>

  
  
<span data-ttu-id="b6d9b-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6d9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6d9b-105">Información para descargar el contenido de una carpeta del servidor durante el [estado descargar tabla](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="b6d9b-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="b6d9b-106">Este proceso de descarga usa la sincronización de cambio incremental (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6d9b-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="b6d9b-107">Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b6d9b-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b6d9b-108">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b6d9b-108">Quick Info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="b6d9b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6d9b-109">Members</span></span>

 <span data-ttu-id="b6d9b-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="b6d9b-110">_cEntNew_</span></span>
  
> <span data-ttu-id="b6d9b-111">[salida] Número de elementos añadidos al almacén local.</span><span class="sxs-lookup"><span data-stu-id="b6d9b-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="b6d9b-112">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b6d9b-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="b6d9b-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="b6d9b-113">_cEntMod_</span></span>
  
> <span data-ttu-id="b6d9b-114">[salida] Número de elementos modificados en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="b6d9b-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="b6d9b-115">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b6d9b-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="b6d9b-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="b6d9b-116">_cEntRead_</span></span>
  
> <span data-ttu-id="b6d9b-117">[salida] Número de elementos leídos o marcados como no leídos en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="b6d9b-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="b6d9b-118">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b6d9b-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="b6d9b-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="b6d9b-119">_cEntDel_</span></span>
  
> <span data-ttu-id="b6d9b-120">[salida] Número de elementos eliminados en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="b6d9b-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="b6d9b-121">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b6d9b-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6d9b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6d9b-122">See also</span></span>



[<span data-ttu-id="b6d9b-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="b6d9b-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b6d9b-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b6d9b-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b6d9b-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="b6d9b-125">DNTBL</span></span>](dntbl.md)

