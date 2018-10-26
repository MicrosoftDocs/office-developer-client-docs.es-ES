---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bd0439c71df7083e3c4787a5d317fa11d2b99c61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578636"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Elimina uno o más mensajes.
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpMsgList_
  
> [entrada] Un puntero a una estructura [ENTRYLIST](entrylist.md) que contiene el número de mensajes para eliminar y una matriz de estructuras [ENTRYID](entryid.md) que identifique los mensajes. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. El parámetro _ulUIParam_ se omite a menos que se establece la marca MESSAGE_DIALOG en el parámetro _ulFlags indicado_ . 
    
 _lpProgress_
  
> [entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI. El parámetro _lpProgress_ se omite a menos que se establece la marca MESSAGE_DIALOG en el parámetro _ulFlags indicado_ . 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se eliminan los mensajes. Se pueden establecer los siguientes indicadores:
    
DELETE_HARD_DELETE
  
> Quita de forma permanente todos los mensajes, incluidos los eliminado temporalmente.
    
MESSAGE_DIALOG 
  
> Muestra un indicador de progreso mientras se realiza la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje especificado o los mensajes se han eliminado correctamente.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todos los mensajes se han eliminado correctamente. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder::DeleteMessages** elimina los mensajes de una carpeta. No se puede eliminar los mensajes que no existen, que se han movido en otra parte, que están abiertos con permiso de lectura y escritura o que se envían actualmente. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando la operación de eliminación implica más de un mensaje, realizar la operación más completo posible para cada carpeta, incluso si no se puede eliminar uno o varios de los mensajes. No detiene la operación de forma prematura a menos que se produzca un error que está fuera de su control, como la falta de memoria, está quedando sin espacio en disco o daños en el almacén de mensajes.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espera a que estos valores devueltos en las siguientes condiciones.
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**DeleteMessages** ha eliminado correctamente todos los mensajes.  <br/> |S_OK  <br/> |
|**DeleteMessages** no pudo eliminar correctamente todos los mensajes y subcarpeta.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** no pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando **DeleteMessages** es no se puede completar, no asuma que se ha realizado ningún trabajo. Es posible que han sido **DeleteMessages** podrá eliminar uno o varios de los mensajes antes de encontrar el error. 
  
 **DeleteMessages** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, según la implementación del almacén de mensajes. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el método **IMAPIFolder::DeleteMessages** para eliminar los mensajes especificados.  <br/> |
   
## <a name="see-also"></a>Vea también



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Usar Macros para el tratamiento de errores](using-macros-for-error-handling.md)

