---
title: IConverterSessionSetTextWrapping
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a8a6546c38c629c193c1978998c95918943fe5c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336634"
---
# <a name="iconvertersessionsettextwrapping"></a>IConverterSession::SetTextWrapping

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el ancho de ajuste de texto de una secuencia MIME que devolverá el convertidor en [IConverterSession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md).
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a>Parameters

 *fWrapText* 
  
> a Si se ajusta o no el texto.
    
 *ulWrapWidth* 
  
> a Ancho del ajuste de texto que se va a usar.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada se realizó correctamente.
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.  <br/> |
   
## <a name="see-also"></a>Vea también



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)


[Constantes MAPI](mapi-constants.md)

