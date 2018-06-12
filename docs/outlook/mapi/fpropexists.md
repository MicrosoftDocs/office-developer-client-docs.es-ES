---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816877"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Se aplica a**: Outlook 
  
Busca una etiqueta de propiedad determinada en una interfaz [IMAPIProp](imapipropiunknown.md) o una interfaz derivada de **IMAPIProp**, como [IMessage](imessageimapiprop.md) o [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Sintaxis

 _pobj_
  
> [entrada] Puntero a la interfaz de **IMAPIProp** o interfaz derivada de **IMAPIProp** dentro de la que se va a buscar la etiqueta de propiedad. 
    
 _ulPropTag_
  
> [entrada] Etiqueta de la propiedad que se va a buscar.
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Se encontró una coincidencia para la etiqueta de la propiedad determinada. 
    
FALSE 
  
> No se encontró una coincidencia para la etiqueta de la propiedad determinada.
    
## <a name="remarks"></a>Notas

Si la etiqueta de propiedad en el parámetro _ulPropTag_ no tiene tipo PT_UNSPECIFIED, la función **FPropExists** busca una coincidencia basándose exclusivamente en el identificador de la propiedad. De lo contrario, la coincidencia es para la etiqueta de propiedad completa, incluido el tipo. 
  

