---
title: Información sobre la API de recuperación de bloqueo de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: fbb6d22414daf3464e80fbf1d9cf92ccb3d560e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576592"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="38530-103">Información sobre la API de recuperación de bloqueo de MAPI</span><span class="sxs-lookup"><span data-stu-id="38530-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="38530-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38530-105">La API de recuperación de MAPI se bloquee comprueba que el estado del archivo de carpetas personales (PST) o archivo de carpetas sin conexión (OST) de memoria para comprobar que los datos están en un estado coherente compartida.</span><span class="sxs-lookup"><span data-stu-id="38530-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="38530-106">Si está en un estado coherente, la función [MAPICrashRecovery](mapicrashrecovery.md) mueve los datos de los archivos pst de abrir u ost en el disco y bloquea los archivos PST u ost y no permitir que cualquier lectura o acceso de escritura a los datos.</span><span class="sxs-lookup"><span data-stu-id="38530-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="38530-107">Esto garantiza que los datos permanecen en un estado coherente hasta que se finalice el proceso.</span><span class="sxs-lookup"><span data-stu-id="38530-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="38530-108">Al garantizar que los archivos PST u ost se encuentran en un estado coherente antes de que finalice el proceso, puede evitar que Microsoft Outlook 2013 y Microsoft Outlook 2010 muestre el siguiente mensaje de error y evitar problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="38530-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="38530-109">**Un archivo de datos no se cerró correctamente la última vez que se usó y que se está protegiendo para problemas. Podría verse afectado el rendimiento mientras la comprobación está en curso.**</span><span class="sxs-lookup"><span data-stu-id="38530-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="38530-110">Esta API ofrece lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="38530-110">This API provides the following:</span></span>
  
<span data-ttu-id="38530-111">Constantes:</span><span class="sxs-lookup"><span data-stu-id="38530-111">Constants:</span></span>
  
- [<span data-ttu-id="38530-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="38530-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="38530-113">Funciones:</span><span class="sxs-lookup"><span data-stu-id="38530-113">Functions:</span></span>
  
- [<span data-ttu-id="38530-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="38530-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="38530-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="38530-115">See also</span></span>



[<span data-ttu-id="38530-116">Usar la API de recuperación de bloqueo de MAPI</span><span class="sxs-lookup"><span data-stu-id="38530-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

