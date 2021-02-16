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
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426075"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
> [entrada] Puntero a una [estructura ENTRYLIST](entrylist.md) que contiene el número de mensajes que se deben eliminar y una matriz de estructuras [ENTRYID](entryid.md) que identifican los mensajes. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. El _parámetro ulUIParam_ se omite a menos que MESSAGE_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _lpProgress_
  
> [entrada] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI. El _parámetro lpProgress_ se omite a menos que MESSAGE_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se eliminan los mensajes. Se pueden establecer las siguientes marcas:
    
DELETE_HARD_DELETE
  
> Elimina permanentemente todos los mensajes, incluidos los eliminados temporalmente.
    
MESSAGE_DIALOG 
  
> Muestra un indicador de progreso a medida que avanza la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje o los mensajes especificados se eliminaron correctamente.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todos los mensajes se han eliminado correctamente. Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta. Para probar esta advertencia, use la **macro HR_FAILED** datos. Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentarios

El **método IMAPIFolder::D eleteMessages** elimina los mensajes de una carpeta. Los mensajes que no existen, que se han movido a otro lugar, que están abiertos con permiso de lectura y escritura o que se envían actualmente no se pueden eliminar. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando la operación de eliminación implica más de un mensaje, realice la operación lo más completa posible para cada carpeta, incluso si uno o varios de los mensajes no se pueden eliminar. No detenga la operación antes de tiempo a menos que se produzca un error que esté fuera de su control, como que se queme la memoria, que se esté quedando sin espacio en disco o que el almacén de mensajes esté dañado.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espere estos valores devueltos en las siguientes condiciones.
  
|**Condition**|**Valor devuelto**|
|:-----|:-----|
|**DeleteMessages ha** eliminado correctamente todos los mensajes.  <br/> |S_OK  <br/> |
|**DeleteMessages** no pudo eliminar correctamente todos los mensajes y subcarpetas.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** no se pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando **DeleteMessages** no se puede completar, no suponga que no se ha realizado ningún trabajo. **Es posible que DeleteMessages** haya podido eliminar uno o varios de los mensajes antes de encontrar el error. 
  
 **DeleteMessages** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, según la implementación del almacén de mensajes. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el **método IMAPIFolder::D eleteMessages** para eliminar los mensajes especificados.  <br/> |
   
## <a name="see-also"></a>Consulte también



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)

