---
title: IConverterSessionSetEncoding
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
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382424"
---
# <a name="iconvertersessionsetencoding"></a>IConverterSession::SetEncoding

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Inicializa la codificación que se utilizará durante la conversión.
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a>Parámetros

_et_
  
> Un valor [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) . Se admiten sólo los valores siguientes: 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>Valor devuelto

E_INVALIDARG
  
> El tipo de codificación pasado no era válido.
    
## <a name="remarks"></a>Comentarios

Llame a **SetEncoding** antes de usar [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para llevar a cabo la conversión. 
  
Use **SetEncoding** para establecer la codificación para sólo el cuerpo del mensaje más externo de un elemento de correo. Microsoft Outlook 2010 y Microsoft Outlook 2013 eligen la codificación para los datos adjuntos individuales. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.  <br/> |
   
## <a name="see-also"></a>Vea también

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [Constantes MAPI](mapi-constants.md)

