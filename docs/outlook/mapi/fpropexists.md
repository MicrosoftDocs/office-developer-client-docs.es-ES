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
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429491"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca una etiqueta de propiedad determinada en una [interfaz IMAPIProp](imapipropiunknown.md) o una interfaz derivada de **IMAPIProp**, como [IMessage](imessageimapiprop.md) o [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parámetros

 _pobj_
  
> [entrada] Puntero a la **interfaz IMAPIProp** o interfaz derivada de **IMAPIProp** en la que se va a buscar la etiqueta de propiedad. 
    
 _ulPropTag_
  
> [entrada] Etiqueta de propiedad para la que se va a buscar.
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Se encontró una coincidencia para la etiqueta de propiedad determinada. 
    
FALSE 
  
> No se encontró una coincidencia para la etiqueta de propiedad determinada.
    
## <a name="remarks"></a>Comentarios

Si la etiqueta de propiedad del  _parámetro ulPropTag_ tiene el tipo PT_UNSPECIFIED, la función **FPropExists** busca una coincidencia basada únicamente en el identificador de propiedad. De lo contrario, la coincidencia es para toda la etiqueta de propiedad, incluido el tipo. 
  

