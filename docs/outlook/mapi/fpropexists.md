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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0d016c83678d9c1c94ee4ad4b8e12723c03f7bda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570439"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parámetros

 _pobj_
  
> [entrada] Puntero a la interfaz de **IMAPIProp** o interfaz derivada de **IMAPIProp** dentro de la que se va a buscar la etiqueta de propiedad. 
    
 _ulPropTag_
  
> [entrada] Etiqueta de la propiedad que se va a buscar.
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Se encontró una coincidencia para la etiqueta de la propiedad determinada. 
    
FALSE 
  
> No se encontró una coincidencia para la etiqueta de la propiedad determinada.
    
## <a name="remarks"></a>Comentarios

Si la etiqueta de propiedad en el parámetro _ulPropTag_ no tiene tipo PT_UNSPECIFIED, la función **FPropExists** busca una coincidencia basándose exclusivamente en el identificador de la propiedad. De lo contrario, la coincidencia es para la etiqueta de propiedad completa, incluido el tipo. 
  

