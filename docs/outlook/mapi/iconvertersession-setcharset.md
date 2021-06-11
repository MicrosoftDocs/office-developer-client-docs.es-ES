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
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336662"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica un conjunto de caracteres opcional que el convertidor MAPI a MIME usa al convertir un mensaje MAPI en una secuencia MIME.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Parameters

 _fApply_
  
> [in] Indica si se va a usar un juego de caracteres específico para la conversión. Establezca este parámetro en **true para** aplicar el juego de caracteres en conversiones posteriores. Establezca este parámetro en **false** si ya no desea aplicar ningún juego de caracteres específico y volver a los valores predeterminados para los mensajes posteriores. 
    
 _hcharset_
  
> [in] Identificador de un conjunto de caracteres definido en mimeole.h de Windows Mail. Especifique **null** para especificar que no desea aplicar ningún juego de caracteres específico. Para valores **que no son nulos,** use una función como [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) para obtener un identificador para el juego de caracteres. 
    
 _csetapplytype_
  
> [in] Indica cómo aplicar un juego de caracteres para convertir un mensaje, tal como se define en mimeole.h de Windows Mail.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada a la función se realiza correctamente.
    
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
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

