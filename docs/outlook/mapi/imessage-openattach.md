---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 48df5362106e849f061b0797736fad82fafa6584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588716"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Se abre un archivo adjunto. 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parámetros

 _ulAttachmentNum_
  
> [entrada] Número de índice de los datos adjuntos para abrir, tal como se almacena en la propiedad de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos. Este número de índice identifica los datos adjuntos en el mensaje y sólo es válido en el contexto del mensaje.
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a los datos adjuntos. Si se pasa NULL da como resultado una interfaz estándar de los datos adjuntos o **IAttach**, que se devuelven. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla cómo se abren los datos adjuntos. Se pueden establecer los siguientes indicadores: 
    
MAPI_BEST_ACCESS 
  
> Solicita que los datos adjuntos se abran con los permisos de red máximo permitidos para el acceso de usuarios y el número máximo de clientes aplicación. Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se deben abrir los datos adjuntos con permisos de lectura y escritura; Si el cliente no tiene acceso de solo lectura, los datos adjuntos se deben abrir con acceso de solo lectura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenAttach** a correctamente, devolver, posiblemente, antes de que los datos adjuntos son completamente disponibles para el cliente de la llamada. Si los datos adjuntos no está disponible, realizar una llamada posterior a él puede provocar un error. 
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los datos adjuntos se abren con acceso de solo lectura y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lppAttach_
  
> [out] Puntero a un puntero a los datos adjuntos abiertos.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los datos adjuntos se abren correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMessage::OpenAttach** abre datos adjuntos de un mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para abrir un archivo adjunto, debe tener acceso a su número de datos adjuntos o la propiedad **PR_ATTACH_NUM** . Llame a [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) para recuperar la tabla de datos adjuntos del mensaje y busque la fila que representa los datos adjuntos que se va a abrir. Para obtener más información, vea [Abrir un archivo adjunto](opening-an-attachment.md) . 
  
No intente abrir un archivo adjunto varias veces; los resultados son dependientes en el proveedor de almacén de mensajes y no definido.
  
Puede solicitar que los datos adjuntos se pueden abrir en modo de lectura y escritura, en lugar del modo de sólo lectura de forma predeterminada. Sin embargo, si los datos adjuntos en realidad se abrirán en modo de lectura y escritura es responsabilidad del proveedor de almacén de mensajes. Puede intentar modificar los datos adjuntos, preparación para controlar posibles errores o comprobar el nivel de acceso que se ha concedido, se recupera la propiedad de **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de los datos adjuntos, si está disponible. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp usado para  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI usa el método **IMessage::OpenAttach** para abrir los objetos de datos adjuntos,  <br/> |
   
## <a name="see-also"></a>Vea también



[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

