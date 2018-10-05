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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391734"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Descomprime el el cuerpo de un mensaje de correo electrónico que está en comprimido con formato (RTF), indica el formato de la secuencia descomprimido, de forma opcional convierte la secuencia descomprimida en su formato nativo y devuelve la secuencia de descomprimido o la convertir la secuencia nativo.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |Msmapi32.dll  <br/> |
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
  
> [entrada] Se trata de un puntero a una secuencia que se abre en la [Propiedad canónico PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) de un mensaje. 
    
_pWCSInfo_
  
> [entrada] Esto es un puntero a un 
    
   Estructura [RTF_WCSINFO](rtf_wcsinfo.md) que contiene las opciones de la función. 
    
_lppUncompressedRTFStream_
  
> [out] Esto es un puntero a la ubicación donde se devuelve una secuencia para el RTF descomprimido. 
    
_pRetInfo_
  
> [out] Se trata de un puntero a una estructura [RTF_WCSRETINFO](rtf_wcsretinfo.md) que contiene información acerca del formato de la secuencia devuelta descomprimida. 
    
## <a name="return-values"></a>Valores devueltos

S_OK 
  
- La llamada a la función es correcta.
    
MAPI_E_INVALID_PARAMETER 
  
- Esto se devuelve si el indicador **MAPI_NATIVE_BODY** se combina con el indicador **MAPI_MODIFY** en el campo **ulFlags** de la estructura **RTF_WCSINFO** señalada a *pWCSInfo* . 
    
## <a name="remarks"></a>Comentarios

**WrapCompressedRTFStreamEx** le permite tener acceso al cuerpo de un mensaje de correo electrónico encapsulado en RTF comprimido por descomprimir la secuencia, devuelve la secuencia descomprimida y su formato y, opcionalmente, la secuencia de cuerpo nativo. La secuencia de cuerpo nativo puede ser en RTF, texto sin formato o HTML. 
  
El modelo de objetos de Microsoft Office Outlook proporciona una propiedad de **cuerpo** para objetos **MailItem** y una [Propiedad MailItem.BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) que indica el formato del texto del cuerpo. Por diseño, una solución que no sea de confianza para Outlook invoca cuadros de diálogo de seguridad generados por la protección de seguridad de Outlook. Uso de la función MAPI exportada **WrapCompressedRTFStreamEx** permite una solución usar MAPI en lugar del modelo de objetos de Outlook y para evitar estos cuadros de diálogo de seguridad. 
  
Debido a que la **MAPI\_NATIVE_BODY** marca no se puede combinar con la **MAPI\_modificar** marca en el campo **ulFlags** de la **RTF\_WCSINFO** estructura señala a *pWCSInfo*, sólo puede tener acceso nativo secuencia de cuerpo en modo de sólo lectura. Para obtener acceso a la secuencia de cuerpo nativos en modo de lectura y escritura, debe utilizar la función **WrapCompressedRTFStream** . 
  
## <a name="see-also"></a>Vea también

- [Recuperar el cuerpo de un mensaje en formato RTF comprimido y convertirlo a su formato nativo](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

