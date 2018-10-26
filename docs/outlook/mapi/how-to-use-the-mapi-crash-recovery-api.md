---
title: Usar la API de recuperación de bloqueo de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: a73889982e4aa72fb664a8eafd6fc8704e581e98
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388507"
---
# <a name="use-the-mapi-crash-recovery-api"></a><span data-ttu-id="9b846-103">Usar la API de recuperación de bloqueo de MAPI</span><span class="sxs-lookup"><span data-stu-id="9b846-103">Use the MAPI Crash Recovery API</span></span>

<span data-ttu-id="9b846-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b846-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b846-105">Este tema contiene un ejemplo de código en C++ que se muestra cómo llamar a la función [MAPICrashRecovery](mapicrashrecovery.md) desde la función [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9b846-105">This topic contains a code sample in C++ that shows how to call the [MAPICrashRecovery](mapicrashrecovery.md) function from the [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) function.</span></span> <span data-ttu-id="9b846-106">La función [MAPICrashRecovery](mapicrashrecovery.md) comprueba que el estado del archivo de carpetas personales (PST) o archivo de carpetas sin conexión (OST) de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="9b846-106">The [MAPICrashRecovery](mapicrashrecovery.md) function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> 

<span data-ttu-id="9b846-107">Si la memoria se encuentra en un estado coherente, la función [MAPICrashRecovery](mapicrashrecovery.md) mueve los datos en el disco y se evita que más acceso de lectura o escritura hasta que se finalice el proceso.</span><span class="sxs-lookup"><span data-stu-id="9b846-107">If the memory is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> <span data-ttu-id="9b846-108">Al garantizar que los archivos PST u ost se encuentran en un estado coherente antes de que finalice el proceso, puede evitar que Microsoft Outlook 2010 o Microsoft Outlook 2013 muestre el siguiente mensaje de error y evitar problemas de rendimiento:</span><span class="sxs-lookup"><span data-stu-id="9b846-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2010 or Microsoft Outlook 2013 from displaying the following error message and avoid performance problems:</span></span> 
  
<span data-ttu-id="9b846-109">**Un archivo de datos no se cerró correctamente la última vez que se usó y que se está protegiendo para problemas. Podría verse afectado el rendimiento mientras la comprobación está en curso.**</span><span class="sxs-lookup"><span data-stu-id="9b846-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
```cpp
LONG WINAPI UnhandledExceptionFilter(__in EXCEPTION_POINTERS* pep) 
{ 
    // Let the OS terminate the process upon return. 
    LONG retval = EXCEPTION_EXECUTE_HANDLER; 
 
    switch (pep->ExceptionRecord->ExceptionCode) 
    { 
        case EXCEPTION_BREAKPOINT: 
        case EXCEPTION_SINGLE_STEP: 
            // Ignore debugging exceptions. 
            retval = EXCEPTION_CONTINUE_SEARCH; 
            break; 
 
        default: 
            // The process is going to be terminated, so disconnect the MAPI database. 
            MAPICrashRecovery(MAPICRASH_RECOVER); 
            // Optionally, you can display a crash reporting dialog box here. 
            // If the user chooses to debug,  
            // call MAPICrashRecovery(MAPICRASH_CONTINUE). 
            break; 
    } 
 
    return retval; 
}
```

## <a name="see-also"></a><span data-ttu-id="9b846-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b846-110">See also</span></span>

- [<span data-ttu-id="9b846-111">Información sobre la API de recuperación de bloqueo de MAPI</span><span class="sxs-lookup"><span data-stu-id="9b846-111">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md) 
- [<span data-ttu-id="9b846-112">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="9b846-112">MAPICrashRecovery</span></span>](mapicrashrecovery.md)

