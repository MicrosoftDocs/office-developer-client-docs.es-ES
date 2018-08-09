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
ms.openlocfilehash: 22f17df9347b4744dfe6598e7007469ffb9e5251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818274"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="a7b5c-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="a7b5c-103">MAPICrashRecovery</span></span>

<span data-ttu-id="a7b5c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7b5c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7b5c-105">La función **MAPICrashRecovery** comprueba que el estado del archivo de carpetas personales (PST) o archivo de carpetas sin conexión (OST) de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="a7b5c-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="a7b5c-106">Si la memoria se encuentra en un estado coherente, la función **MAPICrashRecovery** mueve los datos en el disco y se evita que más acceso de lectura o escritura hasta que se finalice el proceso.</span><span class="sxs-lookup"><span data-stu-id="a7b5c-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a7b5c-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="a7b5c-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7b5c-108">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="a7b5c-108">Exported by:</span></span>  <br/> |<span data-ttu-id="a7b5c-109">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="a7b5c-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="a7b5c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a7b5c-110">Called by:</span></span>  <br/> |<span data-ttu-id="a7b5c-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="a7b5c-111">Client</span></span>  <br/> |
|<span data-ttu-id="a7b5c-112">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="a7b5c-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="a7b5c-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="a7b5c-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="a7b5c-114">Par�metros</span><span class="sxs-lookup"><span data-stu-id="a7b5c-114">Parameters</span></span>

<span data-ttu-id="a7b5c-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7b5c-115">_ulFlags_</span></span>
  
> <span data-ttu-id="a7b5c-116">[entrada] Marcas que se usan para controlar cómo se lleva a cabo la recuperación de errores MAPI.</span><span class="sxs-lookup"><span data-stu-id="a7b5c-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="a7b5c-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="a7b5c-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="a7b5c-118">**MAPICRASH\_recuperar**: si los archivos PST u ost se encuentra en un estado coherente, mover los datos en el disco y bloquear los archivos PST u OST para impedir el acceso de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="a7b5c-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="a7b5c-119">**MAPICRASH\_continuar**: desbloquear los archivos PST u OST para la depuración.</span><span class="sxs-lookup"><span data-stu-id="a7b5c-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="a7b5c-120">Después de una llamada correcta a **MAPICrashRecovery** con la marca **MAPICRASH_RECOVER** , llame a **MAPICrashRecovery** con el **MAPICRASH\_continuar** marca para permitir la depuración continuar.</span><span class="sxs-lookup"><span data-stu-id="a7b5c-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="a7b5c-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: si los archivos PST u ost se encuentra en un estado coherente, mover los datos en el disco y bloquear los archivos PST u OST para impedir el acceso de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="a7b5c-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="a7b5c-122">Los archivos PST u OST no se puede desbloquear con **MAPICRASH\_continuar**.</span><span class="sxs-lookup"><span data-stu-id="a7b5c-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="a7b5c-123">Se debe usar en combinación con **MAPICRASH\_recuperar**.</span><span class="sxs-lookup"><span data-stu-id="a7b5c-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a7b5c-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7b5c-124">Remarks</span></span>

<span data-ttu-id="a7b5c-125">El byte superior (0xFF000000) está reservado para los indicadores de recuperación de bloqueo específico de proveedor.</span><span class="sxs-lookup"><span data-stu-id="a7b5c-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="a7b5c-126">Llamar a **MAPICrashRecovery** con el **MAPICRASH\_recuperar** y los indicadores **MAPICRASH_SYSTEM_SHUTDOWN** en respuesta al mensaje **WM_ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="a7b5c-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7b5c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7b5c-127">See also</span></span>

- [<span data-ttu-id="a7b5c-128">Información sobre la API de recuperación de bloqueo de MAPI</span><span class="sxs-lookup"><span data-stu-id="a7b5c-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="a7b5c-129">Usar la API de recuperación de bloqueo de MAPI</span><span class="sxs-lookup"><span data-stu-id="a7b5c-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

