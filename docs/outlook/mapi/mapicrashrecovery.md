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
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La **función MAPICrashRecovery** comprueba el estado de la memoria compartida del archivo de carpetas personales (PST) o del archivo de carpetas sin conexión (OST). Si la memoria está en un estado coherente, la función **MAPICrashRecovery** mueve los datos al disco y evita el acceso de lectura o escritura hasta que finaliza el proceso. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportado por:  <br/> |olmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Parámetros

_ulFlags_
  
> [entrada] Marcas usadas para controlar cómo se realiza la recuperación de bloqueo de MAPI. Se pueden establecer las siguientes marcas:
    
   - **MAPICRASH \_ RECOVER:** si los ARCHIVOS OST están en un estado coherente, mueva los datos al disco y bloquee los archivos PST o OST para impedir el acceso de lectura o escritura.
    
   - **MAPICRASH \_ CONTINUE:** desbloquea los archivos PST u TS para la depuración. Después de una llamada correcta a **MAPICrashRecovery** con la marca **MAPICRASH_RECOVER,** llame a **MAPICrashRecovery** con la marca **MAPICRASH \_ CONTINUE** para permitir que la depuración continúe. 
    
   - **MAPICRASH \_ SYSTEM_SHUTDOWN:** si los ARCHIVOS OST están en un estado coherente, mueva los datos al disco y bloquee los archivos PST o OST para impedir el acceso de lectura o escritura. Los archivos PST o TS no se pueden desbloquear **con MAPICRASH \_ CONTINUE**. Debe usarse en combinación con **MAPICRASH \_ RECOVER**. 
    
## <a name="remarks"></a>Comentarios

El byte superior (0xFF000000) está reservado para marcas de recuperación de bloqueo específicas del proveedor.
  
Llame **a MAPICrashRecovery** con las marcas RECOVER y **MAPICRASH_SYSTEM_SHUTDOWN** **\_ MAPICRASH** en respuesta al **WM_ENDSESSION** mensaje. 
  
## <a name="see-also"></a>Consulte también

- [Información sobre la API de recuperación de bloqueo de MAPI](about-the-mapi-crash-recovery-api.md)
- [Usar la API de recuperación de bloqueo de MAPI](how-to-use-the-mapi-crash-recovery-api.md)

