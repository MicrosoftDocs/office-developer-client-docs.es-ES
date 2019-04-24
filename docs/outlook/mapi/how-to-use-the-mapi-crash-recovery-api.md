---
title: Usar la API de recuperación de bloqueo de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: a73889982e4aa72fb664a8eafd6fc8704e581e98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346427"
---
# <a name="use-the-mapi-crash-recovery-api"></a>Usar la API de recuperación de bloqueo de MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene un ejemplo de código en C++ que muestra cómo llamar a la función [MAPICrashRecovery](mapicrashrecovery.md) desde la función [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) . La función [MAPICrashRecovery](mapicrashrecovery.md) comprueba el estado del archivo de carpetas personales (PST) o de la memoria compartida del archivo de carpetas sin conexión (OST). 

Si la memoria está en un estado coherente, la función [MAPICrashRecovery](mapicrashrecovery.md) mueve los datos al disco y evita el acceso de lectura o escritura hasta que finaliza el proceso. Al asegurarse de que los archivos PST o OSTs se encuentran en un estado coherente antes de que finalice el proceso, puede evitar que Microsoft Outlook 2010 o Microsoft Outlook 2013 muestren el siguiente mensaje de error y eviten problemas de rendimiento: 
  
**Un archivo de datos no se cerró correctamente la última vez que se usó y se está comprobando para detectar posibles problemas. El rendimiento puede verse afectado mientras la comprobación está en curso.**
  
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

## <a name="see-also"></a>Vea también

- [Información sobre la API de recuperación de bloqueo de MAPI](about-the-mapi-crash-recovery-api.md) 
- [MAPICrashRecovery](mapicrashrecovery.md)

