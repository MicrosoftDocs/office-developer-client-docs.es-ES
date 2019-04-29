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
  
> a Identificador de la ventana primaria del indicador de progreso. El parámetro _ulUIParam_ se omite a menos que se establezca la marca FOLDER_DIALOG en el parámetro _ulFlags_ . 
    
 _lpProgress_
  
> a Un puntero a un objeto Progress que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca FOLDER_DIALOG en el parámetro _ulFlags_ . 
    
 _ulFlags_
  
> a Una máscara de máscara de marcas que controla cómo se vacía la carpeta. Se pueden establecer los siguientes indicadores:
    
DEL_ASSOCIATED 
  
> Elimina todas las subcarpetas, incluidas las subcarpetas que contienen mensajes con contenido asociado. La marca DEL_ASSOCIATED solo tiene significado para la carpeta de nivel superior en la que actúa la llamada.
    
DELETE_HARD_DELETE
  
> Elimina permanentemente todos los mensajes, incluidos los eliminados temporalmente.
    
FOLDER_DIALOG 
  
> Muestra un indicador de progreso mientras se lleva a cabo la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta se vació correctamente.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se realizó correctamente, pero la carpeta no se vació completamente. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder:: EmptyFolder** elimina todo el contenido de una carpeta sin eliminar la carpeta en sí. 
  
Durante una llamada de **EmptyFolder** , no se eliminan los mensajes enviados. 
  
El contenido asociado a una carpeta incluye mensajes que se usan para describir vistas, reglas, formularios personalizados y almacenamiento de soluciones personalizado, y también puede incluir definiciones de formulario. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No llame al método [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para los mensajes de la carpeta que se han enviado. Los mensajes enviados no se eliminan. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espere estos valores devueltos en las siguientes condiciones.
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**EmptyFolder** ha vaciado la carpeta correctamente.  <br/> |S_OK  <br/> |
|**EmptyFolder** no pudo vaciar por completo la carpeta.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** no se pudo completar.  <br/> |Cualquier valor de error  <br/> |
   
Cuando **EmptyFolder** no pueda completarse, no dé por supuesto que no se ha realizado ningún trabajo. Es posible que **EmptyFolder** haya podido eliminar parte del contenido de la carpeta antes de que se produzca el error. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnEmptyFolder  <br/> |MFCMAPI usa el método **IMAPIFolder:: EmptyFolder** para eliminar el contenido de la carpeta especificada.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)

