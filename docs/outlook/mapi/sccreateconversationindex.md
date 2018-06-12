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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 43765cddb2f06bfbe58e0a4000c7eadfdc5f3347
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820585"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Se aplica a**: Outlook 
  
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

## <a name="parameters"></a>Sintaxis

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
    

