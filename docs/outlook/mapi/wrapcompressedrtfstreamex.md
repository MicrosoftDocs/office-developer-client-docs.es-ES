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
  
Descomprime el cuerpo de un mensaje de correo electrónico que está en formato de texto enriquecido comprimido (RTF), indica el formato de la secuencia descomprimida, convierte opcionalmente la secuencia descomprimida a su formato nativo y devuelve la secuencia descomprimida o la secuencia nativa convertida.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |msmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>Parameters

_lpCompressedRTFStream_
  
> [in] Se trata de un puntero a una secuencia que se abre en la propiedad canónica [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) de un mensaje. 
    
_pWCSInfo_
  
> [in] Este es un puntero a un 
    
   [RTF_WCSINFO](rtf_wcsinfo.md) estructura que contiene opciones para la función. 
    
_lppUncompressedRTFStream_
  
> [salida] Este es un puntero a la ubicación donde se devuelve una secuencia para el RTF descomprimido. 
    
_pRetInfo_
  
> [salida] Se trata de un puntero a una [RTF_WCSRETINFO](rtf_wcsretinfo.md) que contiene información sobre el formato de la secuencia descomprimida devuelta. 
    
## <a name="return-values"></a>Valores devueltos

S_OK 
  
- La llamada a la función se realiza correctamente.
    
MAPI_E_INVALID_PARAMETER 
  
- Esto se devuelve si la marca **MAPI_NATIVE_BODY** se combina con la marca **MAPI_MODIFY** en el campo **ulFlags** de la estructura **RTF_WCSINFO** apuntada por  *pWCSInfo*  . 
    
## <a name="remarks"></a>Comentarios

**WrapCompressedRTFStreamEx** permite tener acceso al cuerpo de un mensaje de correo electrónico encapsulado en RTF comprimido descomprimiendo la secuencia, devuelve la secuencia descomprimida y su formato y, opcionalmente, la secuencia de cuerpo nativa. La secuencia de cuerpo nativa puede estar en RTF, texto sin formato o HTML. 
  
El Microsoft Office Outlook de objetos proporciona una propiedad **Body** para objetos **MailItem** y una [propiedad MailItem.BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) que indica el formato del texto del cuerpo. Por diseño, una solución que no es de Outlook invoca cuadros de diálogo de seguridad generados por el Outlook Security Guard. El uso de la función MAPI **exportada WrapCompressedRTFStreamEx** permite que una solución use MAPI en lugar del Outlook de objetos y evite estos cuadros de diálogo de seguridad. 
  
Dado que la marca NATIVE_BODY MAPI no se puede combinar con la marca **MODIFICAR MAPI \_** en el campo **ulFlags** de la estructura **RTF \_ WCSINFO** señalada por *pWCSInfo,* solo puede obtener acceso **\_ a** la secuencia de cuerpo nativa en modo de solo lectura. Para obtener acceso a la secuencia de cuerpo nativa en modo de lectura y escritura, debe usar la **función WrapCompressedRTFStream.** 
  
## <a name="see-also"></a>Vea también

- [Recuperar el cuerpo de un mensaje en RTF comprimido y convertirlo a su formato nativo](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

