---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 03a67371c67d5f0ac346470ec7ab38bb67d5ce2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19817162"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**Hace referencia a**: Outlook 
  
Convierte una secuencia MIME en un mensaje MAPI.
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a>Parámetros

 _pstm_
  
> [entrada] Interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) a una secuencia MIME. 
    
 _pMsg_
  
> [out] Puntero al mensaje que se va a cargar. Vea mapidefs.h para la definición de tipo de **LPMESSAGE**.
    
 _pszSrcSrv_
  
> [entrada] Este valor debe ser **null**.
    
 _ulFlags_
  
> [entrada] Este parámetro identifica ninguna acción especial para que sean tomadas durante la conversión. Debe ser cero (0) si no es ninguna acción específica para que sean tomadas, o una combinación de los siguientes valores:
    
CCSF_EMBEDDED_MESSAGE
  
> Envía/sin enviar información se conserva en sin enviar X.
    
CCSF_SMTP
  
> La secuencia MIME es para un mensaje de Protocolo Simple de transferencia de MAPI (SMTP).
    
CCSF_INCLUDE_BCC
  
> Los destinatarios de CCO de la secuencia MIME se deben incluir en el mensaje MAPI.
    
CCSF_USE_RTF
  
> El cuerpo HTML del objeto stream MIME se debe convertir a formato de texto enriquecido (RTF) en el mensaje MAPI.
    
## <a name="return-value"></a>Valor devuelto

E_INVALIDARG
  
> Indica que _pstm_ es **null**, _pmsg_ es **null**o _ulFlags indicado_ no es válido. 
    
## <a name="remarks"></a>Comentarios

Si ha especificado **CCSF_USE_RTF** como parte de _ulFlags_ y el almacén de mensajes de destino es compatible con HTML y RTF, el mensaje MAPI se convertirá a HTML o RTF. Si el mensaje se convierte en RTF, se va a comprimir el formato convertido RTF, todo el código HTML se incrustarán en la cadena RTF comprimida, y la cadena estarán contenida en la [Propiedad canónico PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.  <br/> |
   
## <a name="see-also"></a>Vea también



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Constantes MAPI](mapi-constants.md)

