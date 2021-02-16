---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Last modified: September 20, 2017'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326948"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte un mensaje MAPI en una secuencia MIME.
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parámetros

 _pmsg_
  
> [entrada] Puntero al mensaje que se convertirá. Vea mapidefs.h para obtener la definición de tipo **de LPMESSAGE**.
    
 _pstm_
  
> [salida] [Interfaz IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para generar la secuencia. 
    
 _ulFlags_
  
>  [entrada] Marcas que indican acciones específicas para el convertidor: 
    
CCSF_8BITHEADERS
  
> El convertidor debe permitir encabezados de 8 bits.
    
CCSF_EMBEDDED_MESSAGE
  
> La información enviada o no enviada se conserva en X-Unsent.
    
CCSF_GLOBAL_MESSAGE
  
> El convertidor debe crear un mensaje internacional (EAI/RFC6530).
    
CCSF_INCLUDE_BCC
  
> Los destinatarios CCO del mensaje MAPI deben incluirse en la secuencia MIME.
    
CCSF_NO_MSGID
  
> No incluya ningún Message-Id en los mensajes salientes.
    
CCSF_NOHEADERS
  
> El convertidor debe omitir los encabezados del mensaje externo.
    
CCSF_PLAIN_TEXT_ONLY
  
> El convertidor solo debe enviar texto sin formato.
    
CCSF_SMTP
  
> Se pasa un mensaje SMTP al convertidor. Esta marca siempre debe establecerse.
    
CCSF_USE_RTF
  
> El convertidor debe convertir el formato HTML a RTF en el mensaje MIME.
    
CCSF_USE_TNEF
  
> El convertidor debe usar el formato TNEF (Transport Neutral Encapsulation Format) en el mensaje MIME.
    
## <a name="return-values"></a>Valores devueltos

E_INVALIDARG
  
> Se han pasado marcas no válidas o  *pmsg*  o  *pstm*  es NULL. 
    
## <a name="remarks"></a>Comentarios

Solo se admite para tipos de mensajes estándar de Outlook.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
  
[Propiedad canónica PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)
  
[Propiedad can�nico de PidLidUseTnef](pidlidusetnef-canonical-property.md)


[Constantes MAPI](mapi-constants.md)

