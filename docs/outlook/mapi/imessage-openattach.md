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
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405901"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un archivo adjunto. 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parameters

 _ulAttachmentNum_
  
> [in] Número de índice de los datos adjuntos que se abrirán, tal como se **almacena** en la propiedad PR_ATTACH_NUM ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Este número de índice identifica de forma única los datos adjuntos del mensaje y solo es válido en el contexto del mensaje.
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a los datos adjuntos. Si se pasa NULL, se devuelve la interfaz estándar de los datos adjuntos o **IAttach.** 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abren los datos adjuntos. Se pueden establecer las siguientes marcas: 
    
MAPI_BEST_ACCESS 
  
> Solicita que los datos adjuntos se abran con los permisos máximos de red permitidos para el usuario y el acceso máximo a la aplicación cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, los datos adjuntos deben abrirse con permiso de lectura y escritura; si el cliente tiene acceso de solo lectura, los datos adjuntos deben abrirse con acceso de solo lectura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que OpenAttach** vuelva correctamente, posiblemente antes de que los datos adjuntos estén totalmente disponibles para el cliente que realiza la llamada. Si los datos adjuntos no están disponibles, realizar una llamada posterior a él puede provocar un error. 
    
MAPI_MODIFY 
  
> Solicitudes de permiso de lectura y escritura. De forma predeterminada, los datos adjuntos se abren con acceso de solo lectura y los clientes no deben funcionar con la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lppAttach_
  
> [salida] Puntero a un puntero a los datos adjuntos abiertos.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los datos adjuntos se abrieron correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMessage::OpenAttach** abre los datos adjuntos de un mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para abrir un archivo adjunto, debe tener acceso a su número de datos adjuntos **o PR_ATTACH_NUM** propiedad. Llama [a IMessage::GetAttachmentTable para](imessage-getattachmenttable.md) recuperar la tabla de datos adjuntos del mensaje y localizar la fila que representa los datos adjuntos que se abrirán. Vea [Abrir datos adjuntos](opening-an-attachment.md) para obtener más información. 
  
No intente abrir un archivo adjunto varias veces; los resultados son indefinidos y dependen del proveedor del almacén de mensajes.
  
Puede solicitar que los datos adjuntos se abran en modo de lectura y escritura, en lugar del modo predeterminado de solo lectura. Sin embargo, si los datos adjuntos se abrirán realmente en modo de lectura y escritura, será el proveedor del almacén de mensajes. Puede intentar modificar los datos adjuntos, prepararse para controlar posibles errores o comprobar el nivel de acceso concedido recuperando la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de los datos adjuntos, si está disponible. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp Se usa para  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI usa el **método IMessage::OpenAttach** para abrir objetos de datos adjuntos,  <br/> |
   
## <a name="see-also"></a>Vea también



[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

