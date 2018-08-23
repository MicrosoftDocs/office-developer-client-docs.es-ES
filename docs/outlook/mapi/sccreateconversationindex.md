---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5ae0c9f123ade599ca9bc1d3bdea3e9c89cfbc16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594155"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica que en un subproceso del mensaje de un mensaje pertenece. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a>Parámetros

 _cbParent_
  
> [entrada] Recuento de bytes en el índice de conversación primario.
    
 _lpbParent_
  
> [entrada] Puntero a bytes en el índice de conversación primario. Esto puede ser NULL si _cbParent_ es cero. 
    
 _lpcbIndex_
  
> [out] Puntero para el número de bytes en el nuevo índice de conversación devuelto por la llamada. 
    
 _lppbIndex_
  
> [out] Puntero a un puntero al nuevo índice de conversación devuelto por la llamada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    

