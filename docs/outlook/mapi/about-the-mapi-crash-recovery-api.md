---
title: Información sobre la API de recuperación de bloqueo de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420265"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="827f0-103">Información sobre la API de recuperación de bloqueo de MAPI</span><span class="sxs-lookup"><span data-stu-id="827f0-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="827f0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="827f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="827f0-105">La API de recuperación de bloqueo MAPI comprueba el estado de la memoria compartida del archivo de carpetas personales (PST) o de carpetas sin conexión (OST) para comprobar que los datos están en un estado coherente.</span><span class="sxs-lookup"><span data-stu-id="827f0-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="827f0-106">Si se encuentra en un estado coherente, la función [MAPICrashRecovery](mapicrashrecovery.md) mueve los datos de los ARCHIVOS PST u UNIDADES de sistema operativo abiertos al disco y bloquea los ARCHIVOSTS u OST y no permite ningún acceso de lectura o escritura a los datos.</span><span class="sxs-lookup"><span data-stu-id="827f0-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="827f0-107">Esto garantiza que los datos permanezcan en un estado coherente hasta que finalice el proceso.</span><span class="sxs-lookup"><span data-stu-id="827f0-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="827f0-108">Al asegurarse de que los PST o los OST están en un estado coherente antes de que finalice el proceso, puede impedir que Microsoft Outlook 2013 y Microsoft Outlook 2010 muestren el siguiente mensaje de error y eviten problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="827f0-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="827f0-109">**Un archivo de datos no se ha cerrado correctamente la última vez que se usó y se está buscando problemas. El rendimiento puede verse afectado mientras la comprobación está en curso.**</span><span class="sxs-lookup"><span data-stu-id="827f0-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="827f0-110">Esta API proporciona lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="827f0-110">This API provides the following:</span></span>
  
<span data-ttu-id="827f0-111">Constantes:</span><span class="sxs-lookup"><span data-stu-id="827f0-111">Constants:</span></span>
  
- [<span data-ttu-id="827f0-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="827f0-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="827f0-113">Funciones:</span><span class="sxs-lookup"><span data-stu-id="827f0-113">Functions:</span></span>
  
- [<span data-ttu-id="827f0-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="827f0-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="827f0-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="827f0-115">See also</span></span>



[<span data-ttu-id="827f0-116">Usar la API de recuperación de bloqueo de MAPI</span><span class="sxs-lookup"><span data-stu-id="827f0-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

