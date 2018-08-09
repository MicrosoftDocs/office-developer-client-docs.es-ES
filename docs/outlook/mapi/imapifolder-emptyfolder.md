---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7d8653b8f0cb2196319c4a9c2b4bca89c8be5a24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817253"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**Hace referencia a**: Outlook 
  
Elimina todos los mensajes y subcarpetas de una carpeta sin eliminar la propia carpeta.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. El parámetro _ulUIParam_ se omite a menos que se establece la marca FOLDER_DIALOG en el parámetro _ulFlags indicado_ . 
    
 _lpProgress_
  
> [entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI. El parámetro _lpProgress_ se omite a menos que se establece la marca FOLDER_DIALOG en el parámetro _ulFlags indicado_ . 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se vacía la carpeta. Se pueden establecer los siguientes indicadores:
    
DEL_ASSOCIATED 
  
> Elimina todas las subcarpetas, incluidas las subcarpetas que contienen los mensajes con contenido asociado. El indicador DEL_ASSOCIATED sólo tiene significado para la llamada actúa en la carpeta de nivel superior.
    
DELETE_HARD_DELETE
  
> Quita de forma permanente todos los mensajes, incluidos los eliminado temporalmente.
    
FOLDER_DIALOG 
  
> Muestra un indicador de progreso mientras se realiza la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta se ha vaciado correctamente.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero la carpeta no estaba totalmente vacía. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder::EmptyFolder** elimina todos los del contenido de una carpeta sin eliminar la propia carpeta. 
  
Durante una llamada **EmptyFolder** , no se eliminan los mensajes enviados. 
  
Contenido asociados de una carpeta incluye los mensajes que se utilizan para describir las vistas, reglas, formularios personalizados y el almacenamiento de soluciones personalizadas y también pueden incluir las definiciones del formulario. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

No llame al método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para los mensajes en la carpeta que se han enviado. No se eliminan los mensajes enviados. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espera a que estos valores devueltos en las siguientes condiciones.
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**EmptyFolder** ha vaciado correctamente la carpeta.  <br/> |S_OK  <br/> |
|**EmptyFolder** no pudo completamente vacíe la carpeta.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** no pudo completar.  <br/> |Cualquier valor de error  <br/> |
   
Cuando no se puede completar **EmptyFolder** , no asuma que se ha realizado ningún trabajo. Es posible que han sido **EmptyFolder** podrá eliminar parte del contenido de la carpeta antes de encontrar el error. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI usa el método **IMAPIFolder::EmptyFolder** para eliminar el contenido de la carpeta especificada.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)

