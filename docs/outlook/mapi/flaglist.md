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
ms.openlocfilehash: f7a236c2a7e307d278cac5ef413cbd2f600bf09f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582101"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de marcas que se usan para indicar el estado de las entradas de dirección durante el proceso de resolución de nombres.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>Members

 **cFlags**
  
> Recuento de indicadores definidas en MAPI en la lista.
    
 **ulFlags**
  
> Una matriz de marcadores que proporciona el estado de la operación de resolución de nombres para un destinatario. Se pueden establecer los siguientes indicadores:
    
MAPI_AMBIGUOUS 
  
> El destinatario se ha resuelto, pero no a un identificador de entrada único. Otros contenedores de la libreta de direcciones no deben intentar resolver este destinatario. 
    
MAPI_RESOLVED 
  
> El destinatario se ha resuelto para un identificador de entrada único. Otros contenedores de la libreta de direcciones no deben intentar resolver este destinatario. 
    
MAPI_UNRESOLVED 
  
> La entrada no se ha resuelta. Otros contenedores de la libreta de direcciones deben intentar resolver a este destinatario.
    
## <a name="remarks"></a>Comentarios

La estructura **FLAGLIST** se usa como un parámetro para [IABContainer:: ResolveNames](iabcontainer-resolvenames.md). Cada uno de los destinatarios que se puede resolver se incluye en una estructura de [ADRLIST](adrlist.md) . Como el contenedor de la libreta de direcciones intenta resolver a cada destinatario, Establece la marca adecuada en la entrada correspondiente en la estructura **FLAGLIST** . Todas las entradas de la estructura de **FLAGLIST** se encuentran en el mismo orden que las entradas de la estructura de **ADRLIST** . Esto facilita la asociar un valor de marca a un destinatario. 
  
## <a name="see-also"></a>Recursos adicionales



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Estructuras MAPI](mapi-structures.md)

