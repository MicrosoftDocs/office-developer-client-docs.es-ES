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
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429197"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica una libreta de direcciones MAPI opcional que el convertidor MAPI a MIME usa para resolver direcciones ambiguas al convertir un mensaje MAPI en una secuencia MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Parameters

 _pab_
  
> [in] Puntero a una [interfaz IAddrBook : IMAPIProp](iaddrbookimapiprop.md) que se usará en la conversión MAPI a MIME. Establezca este parámetro en **null** cuando ya no necesite la libreta de direcciones; esto libera la interfaz y restablece el convertidor para que no use ninguna libreta de direcciones. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada a la función se realiza correctamente.
    
## <a name="remarks"></a>Comentarios

Por lo general, la conversión de un mensaje MAPI a una secuencia MIME no requiere iniciar sesión en un perfil MAPI. Sin embargo, para especificar una libreta de direcciones MAPI para la conversión es necesario iniciar sesión en un perfil para obtener la libreta de direcciones.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.  <br/> |
   
## <a name="see-also"></a>Vea también



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

