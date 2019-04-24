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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325630"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una secuencia de texto en formato de texto enriquecido (RTF) no comprimido a partir del formato comprimido usado en la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>Parameters

 _lpCompressedRTFStream_
  
> a Puntero a una secuencia abierta en la propiedad PR_RTF_COMPRESSED de un mensaje. 
    
 _ulFlags_
  
> a Máscara de máscara de las marcas de opción para la función. Se pueden establecer los siguientes indicadores:
    
MAPI_MODIFY 
  
> Si el cliente pretende leer o escribir la interfaz de secuencia ajustada que se devuelve. 
    
STORE_UNCOMPRESSED_RTF 
  
> El formato RTF sin comprimir debe escribirse en la secuencia a la que apunta _lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> contempla Puntero a la ubicación donde **WrapCompressedRTFStream** devuelve una secuencia para el RTF descomprimido. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Si la marca MAPI_MODIFY se pasa en el parámetro _ulFlags_ , el parámetro _lpCompressedRTFStream_ debe estar ya abierto para lectura y escritura. Nuevo texto RTF sin comprimir se debe escribir en la interfaz de secuencia devuelta en _lpUncompressedRTFStream_. Dado que no es posible anexar la secuencia existente, se debe escribir todo el texto del mensaje. 
  
Si se pasa cero en el parámetro _ulFlags_ , _lpCompressedRTFStream_ puede abrirse en modo de solo lectura. Solo se puede leer todo el texto del mensaje de la interfaz de secuencia devuelta en _lpUncompressedRTFStream_. No se puede iniciar la búsqueda a partir de la mitad de la transmisión. 
  
 **WrapCompressedRTFStream** presupone que el puntero de la secuencia comprimida se establece en el principio de la secuencia. Algunos métodos de OLE **IStream** no son compatibles con la secuencia descomprimida devuelta. Entre estos se incluyen **IStream:: Clone**, **IStream:: LockRegion**, **IStream:: Revert**, **IStream:: Seek**, **IStream:: setSize**, **IStream:: Stat**y **IStream:: UnlockRegion**. Para copiar en toda la secuencia, se necesita un bucle de lectura y escritura. 
  
Debido a que el cliente escribe RTF nuevos en formato sin comprimir, debe usar **WrapCompressedRTFStream**, en lugar de escribir directamente en la secuencia. Los clientes compatibles con RTF deben buscar la marca STORE_UNCOMPRESSED_RTF en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) y pasarla a **WrapCompressed RTFStream** si está establecida. 
  
## <a name="see-also"></a>Vea también



[RTFSync](rtfsync.md)

