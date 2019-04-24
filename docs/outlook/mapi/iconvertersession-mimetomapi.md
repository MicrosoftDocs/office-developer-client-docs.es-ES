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
ms.openlocfilehash: 356f4470be26ae3803a53af1cec34b3ac6eb0cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326932"
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
  
> a Interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) a una secuencia MIME. 
    
 _PMSG_
  
> contempla Puntero al mensaje que se va a cargar. Consulte mapidefs. h para obtener la definición de tipo de **LPMESSAGE**.
    
 _pszSrcSrv_
  
> a Este valor debe ser **nulo**.
    
 _ulFlags_
  
> a Este parámetro identifica cualquier acción especial que deba realizarse durante la conversión. Debe ser cero (0) si no se va a realizar ninguna acción específica o una combinación de los valores siguientes:
    
CCSF_EMBEDDED_MESSAGE
  
> La información enviada/no enviada se conserva en X-no enviado.
    
CCSF_SMTP
  
> La secuencia MIME es para un mensaje de protocolo de transferencia de MAPI simple (SMTP).
    
CCSF_INCLUDE_BCC
  
> Los destinatarios CCO de la secuencia MIME deben incluirse en el mensaje MAPI.
    
CCSF_USE_RTF
  
> El cuerpo HTML de la secuencia MIME debe convertirse a formato de texto enriquecido (RTF) en el mensaje MAPI.

CCSF_GLOBAL_MESSAGE
> El convertidor debe controlar la secuencia MIME como un mensaje Internacional (EAI/RFC6530). No se admite en Outlook 2013.
    
## <a name="return-value"></a>Valor devuelto

E_INVALIDARG
  
> Indica que _pstm_ es **null**, _PMSG_ es **null**o _ulFlags_ no es válido. 
    
## <a name="remarks"></a>Comentarios

Si ha especificado **CCSF_USE_RTF** como parte de _ulFlags_ y el almacén de mensajes de destino admite tanto HTML como RTF, el mensaje MAPI se convertirá en HTML o RTF. Si el mensaje se convierte en RTF, el formato convertido será comprimido RTF, cualquier HTML se incrustará en la cadena RTF comprimida y la cadena se incluirá en la [propiedad canónica PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.  <br/> |
   
## <a name="see-also"></a>Vea también



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Constantes MAPI](mapi-constants.md)

