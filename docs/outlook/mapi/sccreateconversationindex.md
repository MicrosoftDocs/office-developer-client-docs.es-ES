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
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415659"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica el lugar al que pertenece un mensaje en un subproceso de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a>Parameters

 _cbParent_
  
> a Número de bytes en el índice de conversaciones primario.
    
 _lpbParent_
  
> a Puntero a los bytes del índice de conversaciones primario. Puede ser NULL si _cbParent_ es cero. 
    
 _lpcbIndex_
  
> contempla Puntero al número de bytes en el nuevo índice de conversación devuelto por la llamada. 
    
 _lppbIndex_
  
> contempla Puntero a un puntero al nuevo índice de conversación devuelto por la llamada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    

