---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357298"
---
# <a name="mapiinit_0"></a><span data-ttu-id="4bf43-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="4bf43-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="4bf43-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bf43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bf43-105">Transmite opciones a la [función MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="4bf43-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4bf43-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4bf43-106">Header file:</span></span>  <br/> |<span data-ttu-id="4bf43-107">MAPIX. H</span><span class="sxs-lookup"><span data-stu-id="4bf43-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="4bf43-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4bf43-108">Members</span></span>

 <span data-ttu-id="4bf43-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="4bf43-109">**ulVersion**</span></span>
  
> <span data-ttu-id="4bf43-110">Un valor entero que representa el número de versión de la **MAPIINIT_0** estructura.</span><span class="sxs-lookup"><span data-stu-id="4bf43-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="4bf43-111">El **miembro ulVersion** es para la expansión futura y no representa la versión de la interfaz MAPI.</span><span class="sxs-lookup"><span data-stu-id="4bf43-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="4bf43-112">Actualmente, **ulVersion** debe establecerse en MAPI_INIT_VERSION.</span><span class="sxs-lookup"><span data-stu-id="4bf43-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="4bf43-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4bf43-113">**ulFlags**</span></span>
  
> <span data-ttu-id="4bf43-114">Máscara de bits de marcas usada para controlar la inicialización de la sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="4bf43-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="4bf43-115">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="4bf43-115">The following flags can be set:</span></span>
    
<span data-ttu-id="4bf43-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="4bf43-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="4bf43-117">MAPI debe generar notificaciones mediante un subproceso dedicado al control de notificaciones en lugar del primer subproceso usado para llamar **a MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="4bf43-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="4bf43-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="4bf43-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="4bf43-119">El autor de la llamada se ejecuta como un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="4bf43-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="4bf43-120">Los autores de llamadas que no se ejecutan como un servicio de Windows no deben establecer esta marca; Los autores de llamadas que se ejecutan como servicio deben establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="4bf43-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="4bf43-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="4bf43-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="4bf43-122">Establezca la MAPI_NO_COINT para que **MAPIInitialize** no intente inicializar COM con una llamada a [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4bf43-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="4bf43-123">Si se **pasa** una estructura MAPIINIT_0 **a MAPIInitialize** con  _ulFlags_ establecido en MAPI_NO_COINIT, MAPI supondrá que COM ya se ha inicializado y omitirá la llamada a **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="4bf43-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4bf43-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4bf43-124">Remarks</span></span>

<span data-ttu-id="4bf43-125">Los clientes multiproceso deben establecer la MAPI_MULTITHREAD_NOTIFICATIONS cliente.</span><span class="sxs-lookup"><span data-stu-id="4bf43-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="4bf43-126">Si no se establece la marca, se generan notificaciones en el subproceso usado para realizar la primera llamada a **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="4bf43-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="4bf43-127">Para obtener más información acerca de cuándo establecer esta marca y cómo implementar la seguridad de subprocesos en un cliente, vea [Subprocesos en MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="4bf43-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4bf43-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4bf43-128">See also</span></span>



[<span data-ttu-id="4bf43-129">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="4bf43-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="4bf43-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="4bf43-130">MAPI Structures</span></span>](mapi-structures.md)

