---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420888"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve una carpeta de su carpeta principal actual a otra carpeta principal.
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpSrcInterface_
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la carpeta principal de la carpeta que se va a copiar o mover.
    
 _lpSrcFolder_
  
> a Puntero a la carpeta principal de la carpeta que se va a copiar o mover. 
    
 _cbEntryID_
  
> a El recuento de bytes en el identificador de entrada al que apunta _lpEntryID_.
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada de la carpeta que se va a copiar o mover. 
    
 _lpInterface_
  
> a Reserve debe ser NULL.
    
 _lpDestFolder_
  
> a Un puntero a la carpeta que va a recibir la carpeta que se va a copiar o mover.
    
 _lpszNewFolderName_
  
> a Un puntero al nombre de la carpeta copiada o movida; de lo contrario, NULL, que indica que la carpeta copiada o movida debe tener el mismo nombre que la carpeta de origen (la carpeta a la que apunta _lpEntryID_).
    
 _ulUIParam_
  
> a Identificador de la ventana para el cuadro de diálogo indicador de progreso y las ventanas relacionadas. El parámetro _ulUIParam_ se omite a menos que se establezca la marca FOLDER_DIALOG en el parámetro _ulFlags_ . 
    
 _lpProgress_
  
> a Un puntero a un objeto Progress que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca FOLDER_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se realiza la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
COPY_SUBFOLDERS 
  
> Todas las subcarpetas de la carpeta se deben copiar o mover. Cuando COPY_SUBFOLDERS no se establece para una operación de copia, solo se copia la carpeta identificada por _lpEntryID_ . Con una operación de movimiento, el comportamiento de COPY_SUBFOLDERS es el valor predeterminado independientemente de si se ha establecido la marca. 
    
FOLDER_DIALOG 
  
> Solicita la presentación de un indicador de progreso.
    
FOLDER_MOVE 
  
> La carpeta debe moverse en lugar de copiarse. Si no se establece FOLDER_MOVE, se copia la carpeta.
    
MAPI_UNICODE 
  
> El nombre de la carpeta está en formato Unicode. Si no se establece la marca MAPI_UNICODE, el nombre de la carpeta está en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta se ha copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta de la carpeta de destino. El proveedor de almacenamiento de mensajes requiere que los nombres de las carpetas sean únicos. La operación se detiene sin completar.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se realizó correctamente, pero no todas las entradas se copiaron correctamente. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: CopyFolder** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes. Los proveedores de almacenamiento de mensajes pueden llamar a **IMAPISupport:: CopyFolder** en su implementación de [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) para copiar o mover una sola carpeta de una carpeta principal a otra. 
  
 **IMAPISupport:: CopyFolder** agrega la carpeta copiada o movida como una subcarpeta de la carpeta de destino. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **IMAPISupport:: CopyFolder** permite el cambio de nombre y movimiento simultáneo de carpetas y la copia o traslado de subcarpetas de la carpeta afectada. Para copiar o mover todas las subcarpetas anidadas en la carpeta copiada o movida, pase la marca COPY_SUBFOLDERS en _ulFlags_. 
  
Espere los siguientes valores devueltos en las siguientes condiciones:
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**CopyFolder** copió o movió correctamente la carpeta y todas sus subcarpetas, si corresponde.  <br/> |S_OK  <br/> |
|**CopyFolder** no pudo copiar o mover correctamente todas las carpetas.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** no se pudo completar.  <br/> |Cualquier valor de error  <br/> |
   
Si **CopyFolder** devuelve un valor de error, no continúe en el supuesto de que no se ha realizado ningún trabajo. Es posible que una o más carpetas se hayan copiado o movido antes de que **CopyFolder** experimentó el error. 
  
## <a name="see-also"></a>Ver también



[IMAPISupport: IUnknown](imapisupportiunknown.md)

