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
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336417"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de subobjeto que se usa para filtrar las filas de datos adjuntos de un mensaje o la tabla de destinatarios.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>Members

 **ulSubObject**
  
> Tipo de subobjeto que sirve como destino de la restricción. Los valores posibles son los siguientes: 
    
PR_MESSAGE_RECIPIENTS 
  
> Aplique la restricción a la tabla de destinatarios de un mensaje. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Aplique la restricción a la tabla de datos adjuntos de un mensaje. 
    
 **lpRes**
  
> Puntero a una estructura [SRestriction](srestriction.md) . 
    
## <a name="remarks"></a>Comentarios

Las restricciones de subobjeto no son compatibles con todas las tablas. Normalmente, solo las carpetas de contenido de carpeta y los resultados de búsqueda son compatibles con ellas. Por ejemplo, las restricciones de subobjeto se usan para buscar un mensaje que tiene un tipo determinado de datos adjuntos o un destinatario. 
  
Si una implementación no admite restricciones de subobjeto, devuelve MAPI_E_TOO_COMPLEX de sus métodos [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) . 
  
Para obtener una descripción general del funcionamiento de las restricciones, consulte [About Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Vea también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

