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
ms.openlocfilehash: 0c78574f213245a5c30ff589ade824e5c5bd84ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410472"
---
# <a name="imapimessagesitegetstore"></a>IMAPIMessageSite::GetStore

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el almacén de mensajes que contiene el mensaje actual, si existe dicho almacén. Este método devolverá NULL en el parámetro  _ppStore_ para los mensajes incrustados, que se almacenan en otro mensaje en lugar de directamente en un almacén de mensajes. 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a>Parámetros

 _ppStore_
  
> [salida] Puntero a un puntero al almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
S_FALSE 
  
> No hay ningún almacén que contenga el mensaje.
    
## <a name="remarks"></a>Comentarios

Para obtener una lista de interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetStore  <br/> |MFCMAPI usa el **método IMAPIMessageSite::GetStore** para obtener el puntero almacenado actualmente en caché al almacén especificado, si está disponible.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario MAPI](mapi-form-interfaces.md)

