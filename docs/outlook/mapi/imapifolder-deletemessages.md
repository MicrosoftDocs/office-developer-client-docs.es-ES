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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280123"
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

## <a name="parameters"></a>Parameters

 _lpMsgList_
  
> a Un puntero a una estructura [ENTRYLIST](entrylist.md) que contiene el número de mensajes que se va a eliminar y una matriz de estructuras [EntryID](entryid.md) que identifican los mensajes. 
    
 _ulUIParam_
  
> a Identificador de la ventana primaria del indicador de progreso. El parámetro _ulUIParam_ se omite a menos que se establezca la marca MESSAGE_DIALOG en el parámetro _ulFlags_ . 
    
 _lpProgress_
  
> a Un puntero a un objeto Progress que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca MESSAGE_DIALOG en el parámetro _ulFlags_ . 
    
 _ulFlags_
  
> a Una máscara de máscara de marcas que controla cómo se eliminan los mensajes. Se pueden establecer los siguientes indicadores:
    
DELETE_HARD_DELETE
  
> Elimina permanentemente todos los mensajes, incluidos los eliminados temporalmente.
    
MESSAGE_DIALOG 
  
> Muestra un indicador de progreso mientras se lleva a cabo la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje o los mensajes especificados se eliminaron correctamente.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se realizó correctamente, pero no todos los mensajes se eliminaron correctamente. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder::D eletemessages** elimina mensajes de una carpeta. Los mensajes que no existen, que se han movido a otra ubicación, que están abiertos con permisos de lectura y escritura, o que se envían actualmente no se pueden eliminar. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando la operación de eliminación implica más de un mensaje, realice la operación lo más completamente posible para cada carpeta, incluso si uno o más de los mensajes no se pueden eliminar. No detenga la operación prematuramente a menos que se produzca un error que esté más allá del control, como la falta de memoria, la falta de espacio en disco o que esté dañada en el almacén de mensajes.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espere estos valores devueltos en las siguientes condiciones.
  
|**Condition**|**Valor devuelto**|
|:-----|:-----|
|**DeleteMessages** ha eliminado correctamente todos los mensajes.  <br/> |S_OK  <br/> |
|**DeleteMessages** no pudo eliminar correctamente todos los mensajes y subcarpetas.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** no se pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando **DeleteMessages** no pueda completarse, no dé por supuesto que no se ha realizado ningún trabajo. Es posible que **DeleteMessages** haya podido eliminar uno o más mensajes antes de que se produzca el error. 
  
 **DeleteMessages** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, en función de la implementación del almacén de mensajes. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI usa el método **IMAPIFolder::D eletemessages** para eliminar los mensajes especificados.  <br/> |
   
## <a name="see-also"></a>Vea también



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)

