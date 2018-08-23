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
description: 'Última modificación: 20 de septiembre de 2017'
ms.openlocfilehash: bcbc3d21a03c1585288ad23b1fb2d311d686f55c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570453"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte un mensaje MAPI a una secuencia MIME.
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parámetros

 _pMsg_
  
> [entrada] Puntero al mensaje que se va a convertir. Vea mapidefs.h para la definición de tipo de **LPMESSAGE**.
    
 _pstm_
  
> [out] Interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) a la secuencia de salida. 
    
 _ulFlags_
  
>  [entrada] Marcas que muestran las acciones específicas para el convertidor de: 
    
CCSF_8BITHEADERS
  
> El convertidor debe permitir que los encabezados de 8 bits.
    
CCSF_EMBEDDED_MESSAGE
  
> Envía/sin enviar información se conserva en sin enviar X.
    
CCSF_GLOBAL_MESSAGE
  
> El convertidor debe crear un mensaje internacional (EAI/RFC6530).
    
CCSF_INCLUDE_BCC
  
> Los destinatarios de CCO del mensaje MAPI se deben incluir en la secuencia MIME.
    
CCSF_NO_MSGID
  
> Campo de identificador de mensaje no se incluya en los mensajes salientes.
    
CCSF_NOHEADERS
  
> El convertidor debe omitir los encabezados del mensaje externo.
    
CCSF_PLAIN_TEXT_ONLY
  
> El convertidor debe enviar sólo texto sin formato.
    
CCSF_SMTP
  
> El convertidor se pasa un mensaje SMTP. Siempre se debe establecer este indicador.
    
CCSF_USE_RTF
  
> El convertidor debe convertir de HTML a formato RTF en el mensaje MIME.
    
CCSF_USE_TNEF
  
> En el mensaje MIME, el convertidor debe utilizar formato de formato de encapsulación neutro de transporte (TNEF).
    
## <a name="return-values"></a>Valores devueltos

E_INVALIDARG
  
> Se pasaron indicadores no válidos o *pmsg* o *pstm* es NULL. 
    
## <a name="remarks"></a>Comentarios

Admite únicamente para los tipos de mensaje estándar de Outlook.
  
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
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
  
[Propiedad canónica PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)
  
[Propiedad can�nico de PidLidUseTnef](pidlidusetnef-canonical-property.md)


[Constantes MAPI](mapi-constants.md)

