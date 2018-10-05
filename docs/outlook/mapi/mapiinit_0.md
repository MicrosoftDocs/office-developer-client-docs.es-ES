---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391153"
---
# <a name="mapiinit0"></a>MAPIINIT_0

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Transmite las opciones de la función [MAPIInitialize](mapiinitialize.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIX. H  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a>Members

 **ulVersion**
  
> Un valor entero que representa el número de versión de la estructura **MAPIINIT_0** . El miembro **ulVersion** es para la expansión futura y no representan la versión de la interfaz de MAPI. Actualmente, se debe establecer **ulVersion** en MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> La máscara de bits de indicadores que se utilizan para controlar la inicialización de la sesión MAPI. Se pueden establecer los siguientes indicadores:
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI debe generar notificaciones mediante un subproceso dedicado a la administración en lugar del primer subproceso utilizado para llamar **MAPIInitialize**de la notificación.
    
MAPI_NT_SERVICE 
  
> El autor de la llamada se ejecuta como un servicio de Windows. Autores de llamadas que no se ejecutan como un servicio de Windows no debe establecer esta marca; autores de llamadas que se ejecutan como un servicio debe establecer este indicador.
    
MAPI_NO_COINIT
  
> Establecer la marca MAPI_NO_COINT para que no intente inicializar COM con una llamada a [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx) **MAPIInitialize** . Si se pasa una estructura **MAPIINIT_0** **MAPIInitialize** con _ulFlags_ establecida en MAPI_NO_COINIT, MAPI asumirá que COM ya se ha inicializado y pasará por alto la llamada a **CoInitialize**.
    
## <a name="remarks"></a>Comentarios

Los clientes de multiproceso deben establecer la marca MAPI_MULTITHREAD_NOTIFICATIONS. Si no se establece la marca, las notificaciones se generan en el subproceso utilizado para realizar la primera llamada a **MAPIInitialize**. 
  
Para obtener más información acerca de cuándo se debe establecer esta marca y cómo implementar la seguridad de los subprocesos en un cliente, vea [subprocesamiento en MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>Vea también



[MAPIInitialize](mapiinitialize.md)


[Estructuras MAPI](mapi-structures.md)

