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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357298"
---
# <a name="mapiinit_0"></a>MAPIINIT_0

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Transmite opciones a la [función MAPIInitialize.](mapiinitialize.md) 
  
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

## <a name="members"></a>Miembros

 **ulVersion**
  
> Un valor entero que representa el número de versión de la **MAPIINIT_0** estructura. El **miembro ulVersion** es para la expansión futura y no representa la versión de la interfaz MAPI. Actualmente, **ulVersion** debe establecerse en MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> Máscara de bits de marcas usada para controlar la inicialización de la sesión MAPI. Se pueden establecer las siguientes marcas:
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI debe generar notificaciones mediante un subproceso dedicado al control de notificaciones en lugar del primer subproceso usado para llamar **a MAPIInitialize**.
    
MAPI_NT_SERVICE 
  
> El autor de la llamada se ejecuta como un servicio de Windows. Los autores de llamadas que no se ejecutan como un servicio de Windows no deben establecer esta marca; Los autores de llamadas que se ejecutan como servicio deben establecer esta marca.
    
MAPI_NO_COINIT
  
> Establezca la MAPI_NO_COINT para que **MAPIInitialize** no intente inicializar COM con una llamada a [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx). Si se **pasa** una estructura MAPIINIT_0 **a MAPIInitialize** con  _ulFlags_ establecido en MAPI_NO_COINIT, MAPI supondrá que COM ya se ha inicializado y omitirá la llamada a **CoInitialize**.
    
## <a name="remarks"></a>Comentarios

Los clientes multiproceso deben establecer la MAPI_MULTITHREAD_NOTIFICATIONS cliente. Si no se establece la marca, se generan notificaciones en el subproceso usado para realizar la primera llamada a **MAPIInitialize**. 
  
Para obtener más información acerca de cuándo establecer esta marca y cómo implementar la seguridad de subprocesos en un cliente, vea [Subprocesos en MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>Consulte también



[MAPIInitialize](mapiinitialize.md)


[Estructuras MAPI](mapi-structures.md)

