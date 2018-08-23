---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de92a1328eb9a089a7914978ab20ab0bf5c430ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581961"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de objetos secundarios que se usa para filtrar las filas de datos adjuntos o la tabla de destinatarios de un mensaje.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>Members

 **ulSubObject**
  
> Tipo de objeto subcaracterística para que sirva como destino para la restricción. Los valores posibles son los siguientes: 
    
PR_MESSAGE_RECIPIENTS 
  
> Aplicar la restricción a la tabla de destinatarios de un mensaje. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Aplicar la restricción a la tabla de datos adjuntos de un mensaje. 
    
 **lpRes**
  
> Puntero a una estructura [SRestriction](srestriction.md) . 
    
## <a name="remarks"></a>Comentarios

Las restricciones de los objetos secundarios no son compatibles con todas las tablas. Normalmente, las tablas de contenido de carpeta sólo y son compatibles con las carpetas de los resultados de búsqueda. Por ejemplo, las restricciones de los objetos secundarios se usan para encontrar un mensaje que tiene un tipo de datos adjuntos o un destinatario determinado. 
  
Si una implementación no es compatible con las restricciones de los objetos secundarios, devuelve MAPI_E_TOO_COMPLEX desde sus métodos [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) . 
  
Para obtener una descripción general de cómo funcionan las restricciones, vea [Restricciones de sobre](about-restrictions.md). 
  
## <a name="see-also"></a>Recursos adicionales



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

