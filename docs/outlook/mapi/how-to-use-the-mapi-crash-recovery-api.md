---
title: Usar la API de recuperación de bloqueo de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 41d70c2ab94712e40de9011bc752c79d8c859161
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595184"
---
# <a name="use-the-mapi-crash-recovery-api"></a>Usar la API de recuperación de bloqueo de MAPI

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene un ejemplo de código en C++ que se muestra cómo llamar a la función [MAPICrashRecovery](mapicrashrecovery.md) desde la función [UnhandledExceptionFilter](http://msdn.microsoft.com/en-us/library/ms681401%28VS.85%29.aspx) . La función [MAPICrashRecovery](mapicrashrecovery.md) comprueba que el estado del archivo de carpetas personales (PST) o archivo de carpetas sin conexión (OST) de memoria compartida. 

Si la memoria se encuentra en un estado coherente, la función [MAPICrashRecovery](mapicrashrecovery.md) mueve los datos en el disco y se evita que más acceso de lectura o escritura hasta que se finalice el proceso. Al garantizar que los archivos PST u ost se encuentran en un estado coherente antes de que finalice el proceso, puede evitar que Microsoft Outlook 2010 o Microsoft Outlook 2013 muestre el siguiente mensaje de error y evitar problemas de rendimiento: 
  
**Un archivo de datos no se cerró correctamente la última vez que se usó y que se está protegiendo para problemas. Podría verse afectado el rendimiento mientras la comprobación está en curso.**
  
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

