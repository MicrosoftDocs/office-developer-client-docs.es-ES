---
title: IConverterSessionSetSaveFormat
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
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b528d6ef45c02b27f8e07d151793fc338f9af7b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336641"
---
# <a name="iconvertersessionsetsaveformat"></a>IConverterSession::SetSaveFormat

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el formato en el que el convertidor devolverá una secuencia MIME en [IConverterSession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md).
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a>Parameters

_mstSaveFormat_
  
> a Formato de guardado que se va a usar para una secuencia MIME. Para obtener más información, vea el tipo de enumeración [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).
    
  - **SAVE_RFC1521**: usar MIME, que es el valor predeterminado.      
  - **SAVE_RFC822**: usar uuencode.
    
## <a name="return-values"></a>Valores devueltos

S_OK
  
> La llamada se realizó correctamente.
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.  <br/> |
   
## <a name="see-also"></a>Vea también

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetEncoding](iconvertersession-setencoding.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [Constantes MAPI](mapi-constants.md)

