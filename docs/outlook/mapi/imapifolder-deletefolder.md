---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417409"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina una subcarpeta.
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada de la subcarpeta que se eliminará.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. El _parámetro ulUIParam_ se omite a menos FOLDER_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _lpProgress_
  
> [entrada] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI. El  _parámetro lpProgress_ se omite a menos que FOLDER_DIALOG marca esté establecida en  _ulFlags_.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla la eliminación de la subcarpeta. Se pueden establecer las siguientes marcas:
    
DEL_FOLDERS 
  
> Se deben eliminar todas las subcarpetas de la subcarpeta a la que _apunta lpEntryID._ 
    
DEL_MESSAGES 
  
> Todos los mensajes de la subcarpeta que apunta  _lpEntryID_ deben eliminarse. 
    
FOLDER_DIALOG 
  
> Se debe mostrar un indicador de progreso mientras continúa la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta especificada se ha eliminado correctamente.
    
MAPI_E_HAS_FOLDERS 
  
> La subcarpeta que se va a eliminar contiene subcarpetas y no se DEL_FOLDERS marca. No se eliminaron las subcarpetas.
    
MAPI_E_HAS_MESSAGES 
  
> La subcarpeta que se va a eliminar contiene mensajes y no se DEL_MESSAGES marca. La subcarpeta no se eliminó.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todas las entradas se han eliminado correctamente. Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta. Para probar esta advertencia, use la **macro HR_FAILED** datos. Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentarios

El **método IMAPIFolder::D eleteFolder** elimina una subcarpeta. De forma predeterminada, **DeleteFolder** solo funciona en carpetas vacías, pero puedes usarla correctamente en carpetas no vacías estableciendo dos marcas: DEL_FOLDERS y DEL_MESSAGES. Solo se pueden eliminar carpetas o carpetas vacías que establezcan las marcas DEL_FOLDERS y DEL_MESSAGES en la llamada **DeleteFolder.** DEL_FOLDERS permite quitar todas las subcarpetas de la carpeta; DEL_MESSAGES permite quitar todos los mensajes de la carpeta. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando la operación de eliminación implica más de una carpeta, realice la operación lo más completa posible para cada carpeta. A veces, una de las carpetas que se va a eliminar no existe o se ha movido o copiado en otro lugar. No detenga la operación antes de tiempo a menos que se produzca un error que esté fuera de su control, como que se queme la memoria, que se esté quedando sin espacio en disco o que el almacén de mensajes esté dañado.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espere estos valores devueltos en las siguientes condiciones.
  
|**Condition**|**Valor devuelto**|
|:-----|:-----|
|**DeleteFolder** ha eliminado correctamente todos los mensajes y subcarpetas.  <br/> |S_OK  <br/> |
|**DeleteFolder** no pudo eliminar correctamente todos los mensajes y subcarpetas.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** no se pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando **DeleteFolder** no se pueda completar, no suponga que no se ha realizado ningún trabajo. **Es posible que DeleteFolder** haya podido eliminar uno o varios de los mensajes y subcarpetas antes de encontrar el error. 
  
Si no se pueden eliminar una o más subcarpetas, **DeleteFolder** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, en función de la implementación del proveedor del almacén de mensajes. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el **método IMAPIFolder::D eleteFolder** para eliminar carpetas.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

