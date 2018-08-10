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
ms.openlocfilehash: 31b2353b76bbac5cd58cd791f4a289c7dbabdb78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818240"
---
# <a name="mapiinit0"></a><span data-ttu-id="c23c3-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="c23c3-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="c23c3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c23c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c23c3-105">Transmite las opciones de la función [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="c23c3-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c23c3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c23c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="c23c3-107">MAPIX. H</span><span class="sxs-lookup"><span data-stu-id="c23c3-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="c23c3-108">Members</span><span class="sxs-lookup"><span data-stu-id="c23c3-108">Members</span></span>

 <span data-ttu-id="c23c3-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="c23c3-109">**ulVersion**</span></span>
  
> <span data-ttu-id="c23c3-110">Un valor entero que representa el número de versión de la estructura **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="c23c3-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="c23c3-111">El miembro **ulVersion** es para la expansión futura y no representan la versión de la interfaz de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c23c3-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="c23c3-112">Actualmente, se debe establecer **ulVersion** en MAPI_INIT_VERSION.</span><span class="sxs-lookup"><span data-stu-id="c23c3-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="c23c3-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c23c3-113">**ulFlags**</span></span>
  
> <span data-ttu-id="c23c3-114">La máscara de bits de indicadores que se utilizan para controlar la inicialización de la sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="c23c3-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="c23c3-115">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="c23c3-115">The following flags can be set:</span></span>
    
<span data-ttu-id="c23c3-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="c23c3-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="c23c3-117">MAPI debe generar notificaciones mediante un subproceso dedicado a la administración en lugar del primer subproceso utilizado para llamar **MAPIInitialize**de la notificación.</span><span class="sxs-lookup"><span data-stu-id="c23c3-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="c23c3-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="c23c3-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="c23c3-119">El autor de la llamada se ejecuta como un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="c23c3-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="c23c3-120">Autores de llamadas que no se ejecutan como un servicio de Windows no debe establecer esta marca; autores de llamadas que se ejecutan como un servicio debe establecer este indicador.</span><span class="sxs-lookup"><span data-stu-id="c23c3-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="c23c3-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="c23c3-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="c23c3-122">Establecer la marca MAPI_NO_COINT para que no intente inicializar COM con una llamada a [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx) **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="c23c3-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="c23c3-123">Si se pasa una estructura **MAPIINIT_0** **MAPIInitialize** con _ulFlags_ establecida en MAPI_NO_COINIT, MAPI asumirá que COM ya se ha inicializado y pasará por alto la llamada a **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="c23c3-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c23c3-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c23c3-124">Remarks</span></span>

<span data-ttu-id="c23c3-125">Los clientes de multiproceso deben establecer la marca MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="c23c3-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="c23c3-126">Si no se establece la marca, las notificaciones se generan en el subproceso utilizado para realizar la primera llamada a **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="c23c3-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="c23c3-127">Para obtener más información acerca de cuándo se debe establecer esta marca y cómo implementar la seguridad de los subprocesos en un cliente, vea [subprocesamiento en MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="c23c3-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c23c3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c23c3-128">See also</span></span>



[<span data-ttu-id="c23c3-129">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="c23c3-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="c23c3-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="c23c3-130">MAPI Structures</span></span>](mapi-structures.md)
