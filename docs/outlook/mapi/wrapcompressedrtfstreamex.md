---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325777"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Descomprime el cuerpo de un mensaje de correo electrónico en formato de texto enriquecido (RTF) comprimido, indica el formato de la secuencia descomprimida, convierte opcionalmente la secuencia descomprimida a su formato nativo y devuelve la secuencia descomprimida o la secuencia nativa convertida.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportado por:  <br/> |msmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>Parámetros

_lpCompressedRTFStream_
  
> [entrada] Se trata de un puntero a una secuencia que se abre en la propiedad canónica [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) de un mensaje. 
    
_pWCSInfo_
  
> [entrada] Se trata de un puntero a un 
    
   [RTF_WCSINFO](rtf_wcsinfo.md) estructura que contiene opciones para la función. 
    
_lppUncompressedRTFStream_
  
> [salida] Se trata de un puntero a la ubicación donde se devuelve una secuencia para el RTF descomprimido. 
    
_pRetInfo_
  
> [salida] Se trata de un puntero a [una RTF_WCSRETINFO](rtf_wcsretinfo.md) que contiene información sobre el formato de la secuencia descomprimida devuelta. 
    
## <a name="return-values"></a>Valores devueltos

S_OK 
  
- La llamada a la función se realiza correctamente.
    
MAPI_E_INVALID_PARAMETER 
  
- Esto se devuelve si la marca **MAPI_NATIVE_BODY** se combina con la marca **MAPI_MODIFY** en el campo **ulFlags** de la estructura **RTF_WCSINFO** apuntada por  *pWCSInfo*  . 
    
## <a name="remarks"></a>Comentarios

**WrapCompressedRTFStreamEx** te permite acceder al cuerpo de un mensaje de correo electrónico encapsulado en RTF comprimido descomprimiendo la secuencia, devuelve la secuencia descomprimida y su formato y, opcionalmente, la secuencia de cuerpo nativo. La secuencia de cuerpo nativo puede estar en RTF, texto sin formato o HTML. 
  
El Microsoft Office Outlook de objetos proporciona una propiedad **Body** para objetos **MailItem** y una propiedad [MailItem.BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) que indica el formato del texto del cuerpo. Por diseño, una solución en la que Outlook no confía invoca cuadros de diálogo de seguridad generados por la Protección de seguridad de Outlook. El uso de la función MAPI **exportada WrapCompressedRTFStreamEx** permite que una solución use MAPI en lugar del modelo de objetos de Outlook y evite estos cuadros de diálogo de seguridad. 
  
Dado que la marca MAPI NATIVE_BODY no se puede combinar con la marca **MAPI \_ MODIFY** en el campo **ulFlags** de la estructura **RTF \_ WCSINFO** señalada por *pWCSInfo,* solo puede tener acceso **\_ a** la secuencia de cuerpo nativo en modo de solo lectura. Para obtener acceso a la secuencia de cuerpo nativo en modo de lectura y escritura, debes usar la **función WrapCompressedRTFStream.** 
  
## <a name="see-also"></a>Consulte también

- [Recuperar el cuerpo de un mensaje en RTF comprimido y convertirlo a su formato nativo](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

