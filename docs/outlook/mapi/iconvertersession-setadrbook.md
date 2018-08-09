---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e6880a32e30b8f208ce5ba0a2d30e635ff464461
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817164"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**Hace referencia a**: Outlook 
  
Especifica una libreta de direcciones MAPI opcional que usa la MAPI para el convertidor MIME para resolver direcciones ambiguas Cuando se convierte un mensaje MAPI a una secuencia MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Parámetros

 _Libreta personal de direcciones_
  
> [entrada] Puntero a un [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interfaz que se utilizará en la conversión MIME de MAPI. Establezca este parámetro en **null** cuando ya no sea necesaria la libreta de direcciones; Esto libera la interfaz y restablece el convertidor a no utilizar cualquier libreta de direcciones. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada a la función es correcta.
    
## <a name="remarks"></a>Comentarios

Convertir una MAPI mensaje en secuencia MIME normalmente no requiere iniciar sesión en un perfil MAPI. Sin embargo, la especificación de una libreta de direcciones MAPI para la conversión requiere inicio de sesión a un perfil para obtener la libreta de direcciones.
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.  <br/> |
   
## <a name="see-also"></a>Vea también



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

