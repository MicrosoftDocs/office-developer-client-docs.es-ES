---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436212"
---
# <a name="rtfsync"></a>RTFSync

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Garantiza que el texto del mensaje de formato de texto enriquecido (RTF) coincide con la versión de texto sin formato. Es necesario llamar a esta función antes de leer la versión RTF y después de modificar la versión RTF. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de almacenamiento de mensajes compatibles con RTF  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Parameters

_lpMessage_
  
> a Puntero al mensaje que se va a actualizar.
    
_ulFlags_
  
> a Máscara de la máscara usada para indicar que se ha cambiado la versión de texto sin formato o RTF del mensaje. Se pueden establecer los siguientes indicadores:
    
  - RTF_SYNC_BODY_CHANGED: la versión de texto sin formato del mensaje ha cambiado.
      
  - RTF_SYNC_RTF_CHANGED: la versión RTF del mensaje ha cambiado.
    
  Todos los demás bits del parámetro _ulFlags_ están reservados para su uso en el futuro. 
    
_lpfMessageUpdated_
  
> contempla Puntero a una variable que indica si hay un mensaje actualizado. TRUE si hay un mensaje actualizado; de lo contrario, FALSE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Si falta la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) o es false, antes de leer la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), se debe llamar a la función **RTFSync** con el RTF_SYNC_BODY_ Se ha cambiado el conjunto de marcas. 
  
Si la marca STORE_RTF_OK no se establece en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), se debe llamar a esta función con la marca RTF_SYNC_RTF_CHANGED establecida después de modificar **PR_RTF_COMPRESSED**. 
  
Si se han cambiado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) y **PR_RTF_COMPRESSED** , se debe llamar a la función **RTFSync** con ambos marcadores establecidos. 
  
Si el valor del parámetro _lpfMessageUpdated_ se establece en true, se debe llamar al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para el mensaje. Si no se llama a **SaveChanges** , no se guardarán las modificaciones en el mensaje. 
  
Los proveedores de almacenamiento de mensajes pueden usar **RTFSync** para mantener las propiedades **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas. 
  
Para obtener más información, vea [compatibilidad con texto RTF para proveedores de almacenamiento de mensajes](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Ver también

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

