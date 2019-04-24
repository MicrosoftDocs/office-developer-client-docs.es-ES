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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349255"
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
  
> a Número de índice de los datos adjuntos que se van a abrir, tal como se almacena en la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) del adjunto. Este número de Índice identifica de forma exclusiva los datos adjuntos del mensaje y solo es válido en el contexto del mensaje.
    
 _lpInterface_
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a los datos adjuntos. Pasar los resultados NULL en la interfaz estándar de los datos adjuntos, o **IAttach**, que se devuelven. 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abren los datos adjuntos. Se pueden establecer los siguientes indicadores: 
    
MAPI_BEST_ACCESS 
  
> Solicita que los datos adjuntos se abran con los permisos de red máximos permitidos para el usuario y el acceso máximo a la aplicación cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, los datos adjuntos deben abrirse con el permiso de lectura y escritura; Si el cliente tiene acceso de solo lectura, los datos adjuntos deben abrirse con acceso de solo lectura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenAttach** se devuelva correctamente, posiblemente antes de que los datos adjuntos estén completamente disponibles para el cliente que realiza la llamada. Si los datos adjuntos no están disponibles, realizar una llamada posterior al mismo puede provocar un error. 
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. De forma predeterminada, los datos adjuntos se abren con acceso de solo lectura y los clientes no deben trabajar en el supuesto de que se ha concedido el permiso de lectura y escritura. 
    
 _lppAttach_
  
> contempla Puntero a un puntero a los datos adjuntos abiertos.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los datos adjuntos se abrieron correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMessage:: OpenAttach** abre los datos adjuntos de un mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para abrir datos adjuntos, debe tener acceso al número de datos adjuntos o a la propiedad **PR_ATTACH_NUM** . Llame a [IMessage:: GetAttachmentTable](imessage-getattachmenttable.md) para recuperar la tabla de datos adjuntos del mensaje y busque la fila que representa los datos adjuntos que se abrirán. Consulte [apertura de datos](opening-an-attachment.md) adjuntos para obtener más información. 
  
No intente abrir un archivo de datos adjuntos varias veces; los resultados no están definidos y dependen del proveedor de almacenamiento de mensajes.
  
Puede solicitar que los datos adjuntos se abran en modo de lectura y escritura, en lugar del modo predeterminado de solo lectura. Sin embargo, si los datos adjuntos se abrirán realmente en modo de lectura y escritura, dependerá del proveedor del almacén de mensajes. Puede intentar modificar los datos adjuntos, prepararse para controlar posibles errores o comprobar el nivel de acceso que se concedió recuperando la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de los datos adjuntos, si está disponible. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|AttachmentsDlg. cpp usado para  <br/> |CAttachmentsDlg:: OpenItemProp  <br/> |MFCMAPI usa el método **IMessage:: OpenAttach** para abrir objetos Attachment,  <br/> |
   
## <a name="see-also"></a>Vea también



[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

