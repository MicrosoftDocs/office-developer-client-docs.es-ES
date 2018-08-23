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
ms.openlocfilehash: de5c98272c08c469acf23b0ecae7eac0a2d1bfe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592517"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina un archivo adjunto.
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _ulAttachmentNum_
  
> [entrada] Número de índice de los datos adjuntos para eliminar. Éste es el valor de propiedad de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método. El parámetro _ulUIParam_ se omite a menos que se establece la marca ATTACH_DIALOG en el parámetro _ulFlags indicado_ . 
    
 _lpProgress_
  
> [entrada] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante la implementación de objeto de progreso MAPI. El parámetro _lpProgress_ se omite a menos que se establece la marca ATTACH_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla la presentación de una interfaz de usuario. Se puede establecer la marca siguiente:
    
ATTACH_DIALOG 
  
> Solicita la visualización de un indicador de progreso mientras se realiza la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los datos adjuntos se eliminan correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMessage::DeleteAttach** elimina los datos adjuntos de un mensaje. 
  
Un dato adjunto eliminado no se elimina de manera permanente hasta que se ha llamado al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Antes de llamar a **DeleteAttach**, llame al método **IUnknown:: Release** para los datos adjuntos y cada uno de sus secuencias. 
  
Debido a que la eliminación de un archivo adjunto puede ser un proceso largo, **DeleteAttach** proporciona el mecanismo que muestra un indicador de progreso. Puede solicitar la visualización de un indicador de progreso pasando un puntero a su [IMAPIProgress: IUnknown](imapiprogressiunknown.md) implementación o NULL si no tiene una implementación. También debe especificar un identificador de ventana en el parámetro _ulUIParam_ y el indicador ATTACH_DIALOG en el parámetro _ulFlags indicado_ . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el método **IMessage::DeleteAttach** para eliminar los datos adjuntos seleccionados.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

