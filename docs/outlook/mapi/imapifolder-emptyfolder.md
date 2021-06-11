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
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416786"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina todos los mensajes y subcarpetas de una carpeta sin eliminar la carpeta en sí.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Identificador de la ventana principal del indicador de progreso. El _parámetro ulUIParam_ se omite a menos que FOLDER_DIALOG marca esté establecida en _el parámetro ulFlags._ 
    
 _lpProgress_
  
> [in] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI. El _parámetro lpProgress_ se omite a menos que FOLDER_DIALOG marca se establezca en _el parámetro ulFlags._ 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se vacía la carpeta. Se pueden establecer las siguientes marcas:
    
DEL_ASSOCIATED 
  
> Elimina todas las subcarpetas, incluidas las subcarpetas que contienen mensajes con contenido asociado. La marca DEL_ASSOCIATED solo significa para la carpeta de nivel superior en la que actúa la llamada.
    
DELETE_HARD_DELETE
  
> Elimina permanentemente todos los mensajes, incluidos los eliminados temporalmente.
    
FOLDER_DIALOG 
  
> Muestra un indicador de progreso mientras continúa la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta se vació correctamente.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha hecho correctamente, pero la carpeta no se ha vaciado completamente. Cuando se devuelve esta advertencia, la llamada debe controlarse como correcta. Para probar esta advertencia, use la **HR_FAILED** macro. Para obtener más información, vea [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El **método IMAPIFolder::EmptyFolder** elimina todo el contenido de una carpeta sin eliminar la carpeta en sí. 
  
Durante una **llamada EmptyFolder,** los mensajes enviados no se eliminan. 
  
El contenido asociado de una carpeta incluye mensajes que se usan para describir vistas, reglas, formularios personalizados y almacenamiento de soluciones personalizado, y también pueden incluir definiciones de formulario. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No llame al [método IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para los mensajes de la carpeta que se han enviado. Los mensajes enviados no se eliminan. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espere estos valores devueltos en las siguientes condiciones.
  
|**Condition**|**Valor devuelto**|
|:-----|:-----|
|**EmptyFolder** ha vaciado correctamente la carpeta.  <br/> |S_OK  <br/> |
|**EmptyFolder** no pudo vaciar completamente la carpeta.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** no se pudo completar.  <br/> |Cualquier valor de error  <br/> |
   
Cuando **EmptyFolder** no se puede completar, no suponga que no se ha realizado ningún trabajo. Es posible que **EmptyFolder** haya podido eliminar parte del contenido de la carpeta antes de encontrar el error. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI usa el **método IMAPIFolder::EmptyFolder** para eliminar el contenido de la carpeta especificada.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)

