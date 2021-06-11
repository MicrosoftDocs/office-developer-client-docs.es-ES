---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Last modified: September 06, 2019'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160289"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte una secuencia MIME en un mensaje MAPI.
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a>Parameters

 _pstm_
  
> [in] [Interfaz IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) a una secuencia MIME. 
    
 _pmsg_
  
> [in] Puntero al mensaje que se cargará. El autor de la llamada debe proporcionar un mensaje para que la API se rellene, por lo que el objeto debe ir [in]. Vea mapidefs.h para obtener la definición de tipo **de LPMESSAGE**.
    
 _pszSrcSrv_
  
> [in] Este valor debe ser **null**.
    
 _ulFlags_
  
> [in] Este parámetro identifica cualquier acción especial que se debe realizar durante la conversión. Debe ser cero (0) si no se va a realizar ninguna acción específica o una combinación de los siguientes valores:
    
CCSF_EMBEDDED_MESSAGE
  
> La información enviada o no se conserva en X-Unsent.
    
CCSF_SMTP
  
> La secuencia MIME es para un mensaje del Protocolo simple de transferencia de correo (SMTP).
    
CCSF_INCLUDE_BCC
  
> Los destinatarios CCO de la secuencia MIME deben incluirse en el mensaje MAPI.
    
CCSF_USE_RTF
  
> El cuerpo HTML de la secuencia MIME debe convertirse al formato de texto enriquecido (RTF) en el mensaje MAPI.

CCSF_GLOBAL_MESSAGE
> El convertidor debe controlar la secuencia MIME como un mensaje internacional (EAI/RFC6530). No se admite en Outlook 2013.
    
## <a name="return-value"></a>Valor devuelto

E_INVALIDARG
  
> Indica que  _pstm_ es **null,**  _pmsg_ es **null** o  _ulFlags_ no es válido. 
    
## <a name="remarks"></a>Comentarios

Si ha especificado  CCSF_USE_RTF como parte de _ulFlags_ y el almacén de mensajes de destino admite HTML y RTF, el mensaje MAPI se convertirá en HTML o RTF. Si el mensaje se convierte en RTF, el formato convertido se comprimirá RTF, cualquier HTML se incrustará en la cadena RTF comprimida y la cadena se incluirá en la propiedad canónica [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.  <br/> |
   
## <a name="see-also"></a>Vea también



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Constantes MAPI](mapi-constants.md)

