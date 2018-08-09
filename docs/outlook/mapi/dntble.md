---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: 51a79075dac62a051f5a28dbcb70e7d6ff200e65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816749"
---
# <a name="dntble"></a><span data-ttu-id="b3664-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="b3664-103">DNTBLE</span></span>

  
  
<span data-ttu-id="b3664-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3664-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3664-105">Información para descargar el contenido de una carpeta del servidor durante el [estado de la tabla de descarga](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="b3664-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="b3664-106">Este proceso de descarga utiliza sincronización de cambio Incremental (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3664-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="b3664-107">Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b3664-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b3664-108">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b3664-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="b3664-109">Members</span><span class="sxs-lookup"><span data-stu-id="b3664-109">Members</span></span>

 <span data-ttu-id="b3664-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="b3664-110">_cEntNew_</span></span>
  
> <span data-ttu-id="b3664-111">[out] Número de elementos que se agregan al almacén local.</span><span class="sxs-lookup"><span data-stu-id="b3664-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="b3664-112">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b3664-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="b3664-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="b3664-113">_cEntMod_</span></span>
  
> <span data-ttu-id="b3664-114">[out] Número de elementos modificados en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="b3664-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="b3664-115">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b3664-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="b3664-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="b3664-116">_cEntRead_</span></span>
  
> <span data-ttu-id="b3664-117">[out] Número de elementos de lectura o marcados como no leído en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="b3664-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="b3664-118">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b3664-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="b3664-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="b3664-119">_cEntDel_</span></span>
  
> <span data-ttu-id="b3664-120">[out] Número de elementos eliminados en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="b3664-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="b3664-121">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="b3664-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b3664-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3664-122">See also</span></span>



[<span data-ttu-id="b3664-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="b3664-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b3664-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b3664-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b3664-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="b3664-125">DNTBL</span></span>](dntbl.md)

