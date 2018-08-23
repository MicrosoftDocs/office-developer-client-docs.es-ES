---
title: IConverterSessionSetCharSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 69023d2c13037fb52a4d1dc4f7376efbd839aebc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581702"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica que un carácter opcional establece que la MAPI para el uso de convertidor MIME al convertir un mensaje MAPI a una secuencia MIME.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Parámetros

 _fApply_
  
> [entrada] Indica si se debe usar un juego específico para la conversión. Establezca este parámetro en **true** para aplicar el juego de caracteres de las conversiones subsiguientes. Establezca este parámetro en **false** si ya no desea aplicar cualquier juego de caracteres específico y volver a los valores predeterminados para los mensajes subsiguientes. 
    
 _hcharset_
  
> [entrada] Un identificador de un juego de caracteres como se define en mimeole.h de correo de Windows. Especifique **null** para especificar que no desea aplicar cualquier juego de caracteres específico. Para los valores que no son **null** , usar una función como [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) para obtener un identificador para el juego de caracteres. 
    
 _csetapplytype_
  
> [entrada] Indica cómo aplicar un juego de caracteres para convertir un mensaje, como se define en mimeole.h de correo de Windows.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada a la función es correcta.
    
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

