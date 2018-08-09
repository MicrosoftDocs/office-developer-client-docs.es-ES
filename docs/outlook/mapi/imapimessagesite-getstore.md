---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2787150a9fa0fc41e04c58b4a4310ffa844f3743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817350"
---
# <a name="imapimessagesitegetstore"></a>IMAPIMessageSite::GetStore

  
  
**Hace referencia a**: Outlook 
  
Devuelve el almacén de mensajes que contiene el mensaje actual, si existe un almacén de este tipo. Este método devolverá NULL en el parámetro _ppStore_ para mensajes incrustados, que se almacenan en otro mensaje en lugar de hacerlo directamente en un almacén de mensajes. 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a>Parámetros

 _ppStore_
  
> [out] Un puntero a un puntero al almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
S_FALSE 
  
> No hay ningún almacén que contiene el mensaje.
    
## <a name="remarks"></a>Comentarios

Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetStore  <br/> |MFCMAPI usa el método **IMAPIMessageSite::GetStore** para obtener el puntero actualmente en caché para el almacén especificado, si está disponible.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario de MAPI](mapi-form-interfaces.md)

