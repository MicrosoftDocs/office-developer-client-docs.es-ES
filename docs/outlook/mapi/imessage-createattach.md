---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6351be353100649e38a14543a44df5e115c9408b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817652"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**Hace referencia a**: Outlook 
  
Crea un anexo nuevo.
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parámetros

 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al mensaje. Si se pasa NULL da como resultado el mensaje interfaz estándar o **IMessage**, que se devuelven. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla cómo se crean los datos adjuntos. Se puede establecer la marca siguiente:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **CreateAttach** devolver de correctamente, posiblemente antes de que los datos adjuntos están totalmente accesible para el cliente de la llamada. Si los datos adjuntos no está accesible, realizar una llamada posterior a él puede provocar un error. 
    
 _lpulAttachmentNum_
  
> [out] Puntero a un número de índice que identifica los datos adjuntos recién creado. Este número es válido sólo cuando el mensaje está abierto y es la base para la propiedad de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.
    
 _lppAttach_
  
> [out] Puntero a un puntero al objeto abrir datos adjuntos.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los datos adjuntos se ha creado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMessage::CreateAttach** crea un anexo nuevo en un mensaje. Los nuevos datos adjuntos y todas las propiedades que se establecen para él, no están disponibles hasta que un cliente ha llamado (método) [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de los datos adjuntos y el método **IMAPIProp::SaveChanges** del mensaje. 
  
El número de datos adjuntos que señala _lpulAttachmentNum_ es único y válido sólo dentro del contexto del mensaje. Es decir, dos archivos adjuntos en dos mensajes diferentes pueden tener el mismo número mientras no dos archivos adjuntos en el mismo mensaje. 
  
## <a name="see-also"></a>Vea también



[IMessage: IMAPIProp](imessageimapiprop.md)

