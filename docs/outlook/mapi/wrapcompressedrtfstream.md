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
ms.openlocfilehash: 9025bcebdd5e656070b31cd82e6519166a3e3791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821004"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**Hace referencia a**: Outlook 
  
Crea un objeto stream de texto en formato de texto de sin comprimir enriquecido (RTF) desde el formato comprimido utilizado en la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
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
  
> [entrada] Puntero a un objeto stream abierto en la propiedad PR_RTF_COMPRESSED de un mensaje. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores de opción para la función. Se pueden establecer los siguientes indicadores:
    
MAPI_MODIFY 
  
> Si el cliente tiene la intención de lectura o escritura de la interfaz de secuencia ajustada que se devuelve. 
    
STORE_UNCOMPRESSED_RTF 
  
> RTF sin comprimir debe escribirse en la secuencia indicada por _lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> [out] Puntero a la ubicación donde **WrapCompressedRTFStream** devuelve una secuencia para el RTF sin comprimir. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Si la marca MAPI_MODIFY se pasa en el parámetro _ulFlags_ , el parámetro _lpCompressedRTFStream_ ya debe estar abierto para lectura y escritura. Nuevo, sin comprimir texto RTF debe escribirse en la interfaz de la secuencia devuelta en _lpUncompressedRTFStream_. Debido a que no es posible que se anexará la secuencia existente, debe escribir el texto de mensaje completo. 
  
Si se pasa cero en el parámetro _ulFlags_ , a continuación, _lpCompressedRTFStream_ se puede abrir como de solo lectura. Sólo el texto de mensaje completo se puede leer fuera de la interfaz de la secuencia devuelta en _lpUncompressedRTFStream_. No es posible iniciar la mitad de la secuencia de búsqueda. 
  
 **WrapCompressedRTFStream** se da por supuesto que el puntero de comprimido de la secuencia se establece en el principio de la secuencia. Algunos métodos de **IStream** OLE no son compatibles con la secuencia devuelta sin comprimir. Esto incluye **sobre IStream:: Clone**, **IStream:: LockRegion**, **IStream:: Revert**, **IStream:: Seek**, **IStream:: SetSize**, **IStream:: Stat**e **IStream:: UnlockRegion**. Para poder copiar a toda la secuencia, se necesita un bucle de lectura y escritura. 
  
Debido a que el cliente escribe RTF nuevo en formato sin comprimir, que debe usar **WrapCompressedRTFStream**, en lugar de escribir directamente en la secuencia. Los clientes de tener en cuenta RTF deben buscar el indicador STORE_UNCOMPRESSED_RTF en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) y pase al **WrapCompressed RTFStream** si se establece. 
  
## <a name="see-also"></a>Vea también



[RTFSync](rtfsync.md)

