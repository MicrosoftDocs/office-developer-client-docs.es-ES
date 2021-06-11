---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410962"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un verbo MAPI.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a>Members

 **lVerb**
  
> Código que representa el verbo que se pasa a [IMAPIForm::D oVerb](imapiform-doverb.md). Los verbos estándar se definen en el archivo de encabezado Exchform.h.
    
 **szVerbname**
  
> Mostrar el nombre del verbo tal como aparece en el menú del formulario.
    
 **fuFlags**
  
> Marcas para el verbo.
    
 **grfAttribs**
  
> Atributos del verbo. 
    
 **ulFlags**
  
> Marca que indica el formato del nombre para mostrar del verbo. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> El nombre para mostrar está en formato Unicode. Si la MAPI_UNICODE no está establecida, el nombre para mostrar está en formato ANSI.
    
## <a name="remarks"></a>Comentarios

La **estructura SMAPIVerb** se pasa como parámetro en los siguientes métodos: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Vea también



[CbMessageClassArray](cbmessageclassarray.md)


[Estructuras MAPI](mapi-structures.md)

