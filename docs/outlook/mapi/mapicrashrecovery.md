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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357305"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La función **MAPICrashRecovery** comprueba el estado del archivo de carpetas personales (PST) o de la memoria compartida del archivo de carpetas sin conexión (OST). Si la memoria está en un estado coherente, la función **MAPICrashRecovery** mueve los datos al disco y evita el acceso de lectura o escritura hasta que finaliza el proceso. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|ExPortado por:  <br/> |olmapi32. dll  <br/> |
|Llamado por:  <br/> |Client  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Parameters

_ulFlags_
  
> a Marcas usadas para controlar cómo se realiza la recuperación de bloqueo de MAPI. Se pueden establecer los siguientes indicadores:
    
   - **MAPICRASH\_recuperar**: si los archivos PST o OSTs están en un estado coherente, mueva los datos al disco y bloquee los archivos PST o OSTs para evitar el acceso de lectura o escritura.
    
   - **MAPICRASH\_continuar**: Desbloquea los archivos PST o OSTs para la depuración. Tras realizar correctamente una llamada a **MAPICrashRecovery** con la marca **MAPICRASH_RECOVER** , llame a **MAPICrashRecovery** con la marca **MAPICRASH\_continuar** para permitir que la depuración continúe. 
    
   - **MAPICRASH\_SYSTEM_SHUTDOWN**: si los archivos PST o OSTs están en un estado coherente, mueva los datos al disco y bloquee los archivos PST o OSTs para evitar el acceso de lectura o escritura. Los archivos PST o OSTs no se pueden desbloquear mediante **MAPICRASH\_continuar**. Debe usarse en combinación con **MAPICRASH\_Recover**. 
    
## <a name="remarks"></a>Comentarios

El byte superior (0xFF000000) se reserva para los indicadores de recuperación de bloqueo específicos del proveedor.
  
Llame a **MAPICrashRecovery** con las marcas **MAPICRASH\_recuperar** y **MAPICRASH_SYSTEM_SHUTDOWN** en respuesta al mensaje **WM_ENDSESSION** . 
  
## <a name="see-also"></a>Vea también

- [Información sobre la API de recuperación de bloqueo de MAPI](about-the-mapi-crash-recovery-api.md)
- [Usar la API de recuperación de bloqueo de MAPI](how-to-use-the-mapi-crash-recovery-api.md)

