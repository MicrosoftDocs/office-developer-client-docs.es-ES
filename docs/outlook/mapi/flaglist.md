---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412978"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de marcas utilizadas para indicar el estado de las entradas de direcciones durante el proceso de resolución de nombres.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>Members

 **cFlags**
  
> Número de marcas definidas por MAPI en la lista.
    
 **ulFlags**
  
> Matriz de marcadores que proporciona el estado de la operación de resolución de nombres para un destinatario. Se pueden establecer los siguientes indicadores:
    
MAPI_AMBIGUOUS 
  
> Se ha resuelto el destinatario, pero no un identificador de entrada único. Otros contenedores de libretas de direcciones no deben intentar resolver este destinatario. 
    
MAPI_RESOLVED 
  
> El destinatario se ha resuelto en un identificador de entrada único. Otros contenedores de libretas de direcciones no deben intentar resolver este destinatario. 
    
MAPI_UNRESOLVED 
  
> La entrada no se ha resuelto. Otros contenedores de libretas de direcciones deben intentar resolver este destinatario.
    
## <a name="remarks"></a>Comentarios

La estructura **FLAGLIST** se usa como parámetro para [IABContainer:: ResolveNames](iabcontainer-resolvenames.md). Cada uno de los destinatarios que se van a resolver se incluye en una estructura [ADRLIST](adrlist.md) . Como el contenedor de la libreta de direcciones intenta resolver cada destinatario, establece la marca correspondiente en la entrada correspondiente de la estructura **FLAGLIST** . Todas las entradas de la estructura **FLAGLIST** están en el mismo orden que las entradas de la estructura **ADRLIST** . Esto hace que sea más fácil asociar una configuración de marca a un destinatario. 
  
## <a name="see-also"></a>Ver también



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Estructuras MAPI](mapi-structures.md)

