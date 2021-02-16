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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406328"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de subelemento que se usa para filtrar las filas de los datos adjuntos o la tabla de destinatarios de un mensaje.
  
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

## <a name="members"></a>Miembros

 **ulSubObject**
  
> Tipo de sub object que sirve como destino de la restricción. Los valores posibles son los siguientes: 
    
PR_MESSAGE_RECIPIENTS 
  
> Aplicar la restricción a la tabla de destinatarios de un mensaje. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Aplicar la restricción a la tabla de datos adjuntos de un mensaje. 
    
 **lpRes**
  
> Puntero a una [estructura SRestriction.](srestriction.md) 
    
## <a name="remarks"></a>Comentarios

Las restricciones de subelementos no son compatibles con todas las tablas. Normalmente, solo las tablas de contenido de carpetas y las carpetas de resultados de búsqueda las admiten. Por ejemplo, las restricciones de subelementos se usan para buscar un mensaje que tiene un tipo determinado de datos adjuntos o destinatarios. 
  
Si una implementación no admite restricciones de subelementos, devuelve MAPI_E_TOO_COMPLEX de sus métodos [IMAPITable::Restrict](imapitable-restrict.md) o [IMAPITable::FindRow.](imapitable-findrow.md) 
  
Para obtener una explicación general de cómo funcionan las [restricciones,](about-restrictions.md)vea Acerca de las restricciones . 
  
## <a name="see-also"></a>Consulte también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

