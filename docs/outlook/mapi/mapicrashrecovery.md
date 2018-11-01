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
ms.openlocfilehash: 6b07d794a8f54477c6706cb70af60f7f7ef57d49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595345"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
La función **MAPICrashRecovery** comprueba que el estado del archivo de carpetas personales (PST) o archivo de carpetas sin conexión (OST) de memoria compartida. Si la memoria se encuentra en un estado coherente, la función **MAPICrashRecovery** mueve los datos en el disco y se evita que más acceso de lectura o escritura hasta que se finalice el proceso. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |olmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Par�metros

_ulFlags_
  
> [entrada] Marcas que se usan para controlar cómo se lleva a cabo la recuperación de errores MAPI. Se pueden establecer los siguientes indicadores:
    
   - **MAPICRASH\_recuperar**: si los archivos PST u ost se encuentra en un estado coherente, mover los datos en el disco y bloquear los archivos PST u OST para impedir el acceso de lectura o escritura.
    
   - **MAPICRASH\_continuar**: desbloquear los archivos PST u OST para la depuración. Después de una llamada correcta a **MAPICrashRecovery** con la marca **MAPICRASH_RECOVER** , llame a **MAPICrashRecovery** con el **MAPICRASH\_continuar** marca para permitir la depuración continuar. 
    
   - **MAPICRASH\_SYSTEM_SHUTDOWN**: si los archivos PST u ost se encuentra en un estado coherente, mover los datos en el disco y bloquear los archivos PST u OST para impedir el acceso de lectura o escritura. Los archivos PST u OST no se puede desbloquear con **MAPICRASH\_continuar**. Se debe usar en combinación con **MAPICRASH\_recuperar**. 
    
## <a name="remarks"></a>Comentarios

El byte superior (0xFF000000) está reservado para los indicadores de recuperación de bloqueo específico de proveedor.
  
Llamar a **MAPICrashRecovery** con el **MAPICRASH\_recuperar** y los indicadores **MAPICRASH_SYSTEM_SHUTDOWN** en respuesta al mensaje **WM_ENDSESSION** . 
  
## <a name="see-also"></a>Vea también

- [Información sobre la API de recuperación de bloqueo de MAPI](about-the-mapi-crash-recovery-api.md)
- [Usar la API de recuperación de bloqueo de MAPI](how-to-use-the-mapi-crash-recovery-api.md)

