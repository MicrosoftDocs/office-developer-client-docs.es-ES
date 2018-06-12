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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 15cf8ff7e282035ddff53565aa92e81e3886729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817224"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**Se aplica a**: Outlook 
  
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

## <a name="parameters"></a>Sintaxis

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada de la subcarpeta para eliminar.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. El parámetro _ulUIParam_ se omite a menos que se establece la marca FOLDER_DIALOG en el parámetro _ulFlags indicado_ . 
    
 _lpProgress_
  
> [entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI. El parámetro _lpProgress_ se omite a menos que se establece la marca FOLDER_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la eliminación de la subcarpeta. Se pueden establecer los siguientes indicadores:
    
DEL_FOLDERS 
  
> Se deben eliminar todas las subcarpetas de la subcarpeta indicada por _lpEntryID_ . 
    
DEL_MESSAGES 
  
> Se deben eliminar todos los mensajes en la subcarpeta que señala _lpEntryID_ . 
    
FOLDER_DIALOG 
  
> Debe mostrarse un indicador de progreso mientras se realiza la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta especificada se ha eliminado correctamente.
    
MAPI_E_HAS_FOLDERS 
  
> La subcarpeta que se va a eliminar contiene las subcarpetas y no se ha establecido el indicador DEL_FOLDERS. No se han eliminado las subcarpetas.
    
MAPI_E_HAS_MESSAGES 
  
> La subcarpeta que se va a eliminar contiene los mensajes, y no se ha establecido el indicador DEL_MESSAGES. No se ha eliminado la subcarpeta.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todas las entradas se eliminaron correctamente. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Notas

El método **IMAPIFolder::DeleteFolder** elimina una subcarpeta. De forma predeterminada, **DeleteFolder** sólo funciona en las carpetas vacías, pero se puede usar correctamente en las carpetas no vacías mediante la configuración de dos indicadores: DEL_FOLDERS y DEL_MESSAGES. Sólo carpetas vacías o carpetas que establecer los indicadores de la DEL_FOLDERS y la DEL_MESSAGES en la llamada **DeleteFolder** se pueden eliminar. DEL_FOLDERS habilita todas las subcarpetas de la carpeta que se va a quitar; DEL_MESSAGES permite que todos los mensajes de la carpeta que se va a quitar. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Cuando la operación de eliminación implica más de una carpeta, realizar la operación más completo posible para cada carpeta. En ocasiones, una de las carpetas que se va a eliminar no existe o se haya movido o copiado en otro lugar. No detiene la operación de forma prematura a menos que se produzca un error que está fuera de su control, como la falta de memoria, está quedando sin espacio en disco o daños en el almacén de mensajes.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espera a que estos valores devueltos en las siguientes condiciones.
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**DeleteFolder** ha eliminado correctamente todos los mensajes y subcarpeta.  <br/> |S_OK  <br/> |
|**DeleteFolder** no pudo eliminar correctamente todos los mensajes y subcarpeta.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** no pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando no se puede completar **DeleteFolder** , no asuma que se ha realizado ningún trabajo. Es posible que han sido **DeleteFolder** podrá eliminar uno o varios de los mensajes y subcarpetas antes de encontrar el error. 
  
Si no se puede eliminar una o varias subcarpetas, **DeleteFolder** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, dependiendo de la implementación del proveedor de almacén de mensajes. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el método **IMAPIFolder::DeleteFolder** para eliminar las carpetas.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

