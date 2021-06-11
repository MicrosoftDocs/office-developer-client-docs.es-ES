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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430710"
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
  
> [in] Número de índice de los datos adjuntos que se eliminarán. Este es el valor de la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
    
 _ulUIParam_
  
> [in] Controla la ventana principal de los cuadros de diálogo o ventanas que muestra este método. El _parámetro ulUIParam_ se omite a menos que ATTACH_DIALOG marca esté establecida en _el parámetro ulFlags._ 
    
 _lpProgress_
  
> [in] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI. El  _parámetro lpProgress_ se omite a menos que ATTACH_DIALOG marca se establezca en  _ulFlags_.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla la presentación de una interfaz de usuario. Se puede establecer la siguiente marca:
    
ATTACH_DIALOG 
  
> Solicita la presentación de un indicador de progreso a medida que avanza la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los datos adjuntos se eliminaron correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMessage::D eleteAttach** elimina los datos adjuntos de un mensaje. 
  
Los datos adjuntos eliminados no se eliminan permanentemente hasta que se haya llamado al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Antes de llamar **a DeleteAttach,** llama al **método IUnknown::Release** para los datos adjuntos y cada una de sus secuencias. 
  
Dado que la eliminación de datos adjuntos puede ser un proceso largo, **DeleteAttach** proporciona el mecanismo que muestra un indicador de progreso. Puede solicitar la presentación de un indicador de progreso pasando un puntero a [su IMAPIProgress : Implementación IUnknown](imapiprogressiunknown.md) o NULL si no tiene una implementación. También debe especificar un identificador de ventana en el _parámetro ulUIParam_ y la marca ATTACH_DIALOG en el _parámetro ulFlags._ 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el **método IMessage::D eleteAttach** para eliminar los datos adjuntos seleccionados.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

