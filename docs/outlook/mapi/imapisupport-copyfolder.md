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

## <a name="parameters"></a>Parámetros

 _lpSrcInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta principal de la carpeta que se va a copiar o mover.
    
 _lpSrcFolder_
  
> [entrada] Puntero a la carpeta principal de la carpeta que se va a copiar o mover. 
    
 _cbEntryID_
  
> [entrada] El recuento de bytes en el identificador de entrada al que apunta  _lpEntryID_.
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada de la carpeta que se va a copiar o mover. 
    
 _lpInterface_
  
> [entrada] Reservado; debe ser NULL.
    
 _lpDestFolder_
  
> [entrada] Puntero a la carpeta que va a recibir la carpeta que se va a copiar o mover.
    
 _lpszNewFolderName_
  
> [entrada] Puntero al nombre de la carpeta copiada o movida; de lo contrario, NULL, que indica que la carpeta copiada o movida debe tener el mismo nombre que la carpeta de origen (la carpeta a la que  _apunta lpEntryID_).
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana para el cuadro de diálogo del indicador de progreso y las ventanas relacionadas. El _parámetro ulUIParam_ se omite a menos FOLDER_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _lpProgress_
  
> [entrada] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI. El  _parámetro lpProgress_ se omite a menos que FOLDER_DIALOG marca esté establecida en  _ulFlags_.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se realiza la operación de copia o movimiento. Se pueden establecer las siguientes marcas:
    
COPY_SUBFOLDERS 
  
> Todas las subcarpetas de la carpeta deben copiarse o moverse. Cuando COPY_SUBFOLDERS no se establece para una operación de copia, solo se copia la carpeta identificada por _lpEntryID._ Con una operación de movimiento, COPY_SUBFOLDERS comportamiento predeterminado independientemente de si se establece la marca. 
    
FOLDER_DIALOG 
  
> Solicita la presentación de un indicador de progreso.
    
FOLDER_MOVE 
  
> La carpeta debe moverse en lugar de copiarse. Si FOLDER_MOVE no se establece, se copia la carpeta.
    
MAPI_UNICODE 
  
> El nombre de la carpeta está en formato Unicode. Si no MAPI_UNICODE marca, el nombre de la carpeta está en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta se ha copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta de la carpeta de destino. El proveedor del almacén de mensajes requiere que los nombres de carpeta sean únicos. La operación se detiene sin completarse.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todas las entradas se han copiado correctamente. Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta. Para probar esta advertencia, use la **macro HR_FAILED** datos. Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::CopyFolder** se implementa para objetos de compatibilidad del proveedor de al almacenamiento de mensajes. Los proveedores de almacenamiento de mensajes pueden llamar a **IMAPISupport::CopyFolder** en su implementación de [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) para copiar o mover una sola carpeta de una carpeta principal a otra. 
  
 **IMAPISupport::CopyFolder** agrega la carpeta copiada o movida como subcarpeta de la carpeta de destino. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **IMAPISupport::CopyFolder** permite cambiar el nombre y mover las carpetas simultáneamente y copiar o mover subcarpetas de la carpeta afectada. Para copiar o mover todas las subcarpetas anidadas en la carpeta copiada o movida, pase la marca COPY_SUBFOLDERS en  _ulFlags_. 
  
Espere los siguientes valores devueltos en las siguientes condiciones:
  
|**Condition**|**Valor devuelto**|
|:-----|:-----|
|**CopyFolder** copió o movió correctamente la carpeta y todas sus subcarpetas, si procede.  <br/> |S_OK  <br/> |
|**CopyFolder** no pudo copiar o mover correctamente todas las carpetas.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** no se pudo completar.  <br/> |Cualquier valor de error  <br/> |
   
Si **CopyFolder** devuelve un valor de error, no continúe con la suposición de que no se ha realizado ningún trabajo. Una o varias carpetas se podrían haber copiado o movido antes de **que CopyFolder** experimentara el error. 
  
## <a name="see-also"></a>Consulte también



[IMAPISupport: IUnknown](imapisupportiunknown.md)

