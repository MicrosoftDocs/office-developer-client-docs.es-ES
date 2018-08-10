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
ms.openlocfilehash: f6afa890f61bb2f394e3cf69e0f2c54699a2ad9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820555"
---
# <a name="rtfsync"></a>RTFSync

**Hace referencia a**: Outlook 
  
Se asegura de que el texto del mensaje de formato de texto enriquecido (RTF) coincide con la versión de texto sin formato. Es necesario llamar a esta función antes de leer la versión RTF y después de modificar la versión RTF. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de almacén de mensajes y aplicaciones cliente de RTF  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Parámetros

_lpMessage_
  
> [entrada] Puntero al mensaje que se van a actualizar.
    
_ulFlags_
  
> [entrada] Máscara de bits de indicadores que se utilizan para indicar la versión de texto sin formato del mensaje o RTF ha cambiado. Se pueden establecer los siguientes indicadores:
    
  - RTF_SYNC_BODY_CHANGED: Ha cambiado la versión de texto sin formato del mensaje.
      
  - RTF_SYNC_RTF_CHANGED: Ha cambiado la versión RTF del mensaje.
    
  Todos los demás bits en el parámetro _ulFlags_ están reservados para uso futuro. 
    
_lpfMessageUpdated_
  
> [out] Puntero a una variable que indica si hay un mensaje actualizado. Es TRUE si hay un mensaje actualizado, FALSE en caso contrario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Si la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) falta o es FALSE, antes de leer la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) en la función **RTFSync** se debe llamar con el RTF_SYNC_BODY_ Puede cambiar el conjunto de marca. 
  
Si no está establecido el indicador STORE_RTF_OK en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), esta función se debe llamar con el indicador RTF_SYNC_RTF_CHANGED establecer después de modificar **PR_RTF_COMPRESSED**. 
  
Si se han cambiado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) y **PR_RTF_COMPRESSED** , debe llamar a la función **RTFSync** con ambos conjunto de indicadores. 
  
Si el valor del parámetro _lpfMessageUpdated_ se establece en TRUE, el método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) debe llamarse para el mensaje. Si no se llama a **SaveChanges** , las modificaciones no se guardarán en el mensaje. 
  
Los proveedores de almacén de mensajes pueden utilizar **RTFSync** para mantener las propiedades **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas. 
  
Para obtener más información, vea [Compatibilidad con texto RTF para los proveedores de almacén de mensajes](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>Vea también

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

