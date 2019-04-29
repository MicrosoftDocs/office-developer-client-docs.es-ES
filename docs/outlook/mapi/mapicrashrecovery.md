---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407217"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="98807-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="98807-103">MAPICrashRecovery</span></span>

<span data-ttu-id="98807-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98807-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98807-105">La función **MAPICrashRecovery** comprueba el estado del archivo de carpetas personales (PST) o de la memoria compartida del archivo de carpetas sin conexión (OST).</span><span class="sxs-lookup"><span data-stu-id="98807-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="98807-106">Si la memoria está en un estado coherente, la función **MAPICrashRecovery** mueve los datos al disco y evita el acceso de lectura o escritura hasta que finaliza el proceso.</span><span class="sxs-lookup"><span data-stu-id="98807-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="98807-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="98807-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98807-108">ExPortado por:</span><span class="sxs-lookup"><span data-stu-id="98807-108">Exported by:</span></span>  <br/> |<span data-ttu-id="98807-109">olmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="98807-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="98807-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="98807-110">Called by:</span></span>  <br/> |<span data-ttu-id="98807-111">Client</span><span class="sxs-lookup"><span data-stu-id="98807-111">Client</span></span>  <br/> |
|<span data-ttu-id="98807-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="98807-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="98807-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="98807-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="98807-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="98807-114">Parameters</span></span>

<span data-ttu-id="98807-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98807-115">_ulFlags_</span></span>
  
> <span data-ttu-id="98807-116">a Marcas usadas para controlar cómo se realiza la recuperación de bloqueo de MAPI.</span><span class="sxs-lookup"><span data-stu-id="98807-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="98807-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="98807-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="98807-118">**MAPICRASH\_recuperar**: si los archivos PST o OSTs están en un estado coherente, mueva los datos al disco y bloquee los archivos PST o OSTs para evitar el acceso de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="98807-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="98807-119">**MAPICRASH\_continuar**: Desbloquea los archivos PST o OSTs para la depuración.</span><span class="sxs-lookup"><span data-stu-id="98807-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="98807-120">Tras realizar correctamente una llamada a **MAPICrashRecovery** con la marca **MAPICRASH_RECOVER** , llame a **MAPICrashRecovery** con la marca **MAPICRASH\_continuar** para permitir que la depuración continúe.</span><span class="sxs-lookup"><span data-stu-id="98807-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="98807-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: si los archivos PST o OSTs están en un estado coherente, mueva los datos al disco y bloquee los archivos PST o OSTs para evitar el acceso de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="98807-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="98807-122">Los archivos PST o OSTs no se pueden desbloquear mediante **MAPICRASH\_continuar**.</span><span class="sxs-lookup"><span data-stu-id="98807-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="98807-123">Debe usarse en combinación con **MAPICRASH\_Recover**.</span><span class="sxs-lookup"><span data-stu-id="98807-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="98807-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98807-124">Remarks</span></span>

<span data-ttu-id="98807-125">El byte superior (0xFF000000) se reserva para los indicadores de recuperación de bloqueo específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="98807-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="98807-126">Llame a **MAPICrashRecovery** con las marcas **MAPICRASH\_recuperar** y **MAPICRASH_SYSTEM_SHUTDOWN** en respuesta al mensaje **WM_ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="98807-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="98807-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="98807-127">See also</span></span>

- [<span data-ttu-id="98807-128">Información sobre la API de recuperación de bloqueo de MAPI</span><span class="sxs-lookup"><span data-stu-id="98807-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="98807-129">Usar la API de recuperación de bloqueo de MAPI</span><span class="sxs-lookup"><span data-stu-id="98807-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

