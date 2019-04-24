---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351082"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina datos adjuntos.
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulAttachmentNum_
  
> a Número de índice de los datos adjuntos que se van a eliminar. Este es el valor de la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.
    
 _ulUIParam_
  
> a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que este método muestra. El parámetro _ulUIParam_ se omite a menos que se establezca la marca ATTACH_DIALOG en el parámetro _ulFlags_ . 
    
 _lpProgress_
  
> a Puntero a un objeto Progress que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca ATTACH_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla la presentación de una interfaz de usuario. Se puede establecer la siguiente marca:
    
ATTACH_DIALOG 
  
> Solicita la visualización de un indicador de progreso mientras se lleva a cabo la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los datos adjuntos se eliminaron correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMessage::D eleteattach** elimina datos adjuntos desde dentro de un mensaje. 
  
Los datos adjuntos eliminados no se eliminan permanentemente hasta que se llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Antes de llamar a **DeleteAttach**, llame al método **IUnknown:: Release** para los datos adjuntos y cada una de sus secuencias. 
  
Como la eliminación de datos adjuntos puede ser un proceso prolongado, **DeleteAttach** proporciona el mecanismo que muestra un indicador de progreso. Puede solicitar la presentación de un indicador de progreso pasando un puntero a su [método imapiprogress:](imapiprogressiunknown.md) implementación de IUNKNOWN o null si no tiene una implementación. También debe especificar un identificador de ventana en el parámetro _ulUIParam_ y la marca ATTACH_DIALOG en el parámetro _ulFlags_ . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|AttachmentsDlg. cpp  <br/> |CAttachmentsDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI usa el método **IMessage::D eleteattach** para eliminar los datos adjuntos seleccionados.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

