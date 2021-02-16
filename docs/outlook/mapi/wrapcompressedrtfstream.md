---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439803"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una secuencia de texto en formato de texto enriquecido (RTF) sin comprimir a partir del formato comprimido usado en la **propiedad PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>Parámetros

 _lpCompressedRTFStream_
  
> [entrada] Puntero a una secuencia abierta en la PR_RTF_COMPRESSED propiedad de un mensaje. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas de opción para la función. Se pueden establecer las siguientes marcas:
    
MAPI_MODIFY 
  
> Indica si el cliente tiene la intención de leer o escribir la interfaz de secuencia ajustada que se devuelve. 
    
STORE_UNCOMPRESSED_RTF 
  
> Rtf sin comprimir debe escribirse en la secuencia a la que  _apunta lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> [salida] Puntero a la ubicación donde **WrapCompressedRTFStream** devuelve una secuencia para el RTF sin comprimir. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Si la MAPI_MODIFY se pasa en el parámetro  _ulFlags,_ el parámetro  _lpCompressedRTFStream_ ya debe estar abierto para lectura y escritura. El texto RTF nuevo y sin comprimir debe escribirse en la interfaz de secuencia devuelta  _en lpUncompressedRTFStream_. Dado que no es posible anexar la secuencia existente, se debe escribir todo el texto del mensaje. 
  
Si se pasa cero en el  _parámetro ulFlags,_ es posible que  _lpCompressedRTFStream_ se abra como de solo lectura. Solo se puede leer todo el texto del mensaje de la interfaz de secuencia devuelta  _en lpUncompressedRTFStream_. No es posible buscar empezando en medio de la secuencia. 
  
 **WrapCompressedRTFStream** supone que el puntero de la secuencia comprimida está establecido al principio de la secuencia. Algunos métodos **OLE IStream** no son compatibles con la secuencia sin comprimir devuelta. Estos incluyen **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat** e **IStream::UnlockRegion**. Para copiar a toda la secuencia, se necesita un bucle de lectura y escritura. 
  
Dado que el cliente escribe nuevo RTF en formato sin comprimir, debe usar **WrapCompressedRTFStream**, en lugar de escribir directamente en la secuencia. Los clientes compatibles con RTF deben buscar la marca STORE_UNCOMPRESSED_RTF en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) y pasarla a **WrapCompressed RTFStream** si está establecida. 
  
## <a name="see-also"></a>Consulte también



[RTFSync](rtfsync.md)

