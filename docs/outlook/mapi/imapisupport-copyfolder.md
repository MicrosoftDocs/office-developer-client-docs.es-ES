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
  
Copia o mueve una carpeta de su carpeta principal actual a otra carpeta primaria.
  
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
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta principal de la carpeta que se va a copiar o mover.
    
 _lpSrcFolder_
  
> [in] Puntero a la carpeta principal de la carpeta que se va a copiar o mover. 
    
 _cbEntryID_
  
> [in] Recuento de bytes en el identificador de entrada señalado por  _lpEntryID_.
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada de la carpeta que se va a copiar o mover. 
    
 _lpInterface_
  
> [in] Reservado; debe ser NULL.
    
 _lpDestFolder_
  
> [in] Puntero a la carpeta que va a recibir la carpeta que se va a copiar o mover.
    
 _lpszNewFolderName_
  
> [in] Puntero al nombre de la carpeta copiada o movida; en caso contrario, NULL, que indica que la carpeta copiada o movida debe tener el mismo nombre que la carpeta de origen (la carpeta a la que  _apunta lpEntryID_).
    
 _ulUIParam_
  
> [in] Un identificador de la ventana para el cuadro de diálogo del indicador de progreso y las ventanas relacionadas. El _parámetro ulUIParam_ se omite a menos que FOLDER_DIALOG marca esté establecida en _el parámetro ulFlags._ 
    
 _lpProgress_
  
> [in] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI. El  _parámetro lpProgress_ se omite a menos que FOLDER_DIALOG marca se establezca en  _ulFlags_.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se realiza la operación de copiar o mover. Se pueden establecer las siguientes marcas:
    
COPY_SUBFOLDERS 
  
> Todas las subcarpetas de la carpeta se deben copiar o mover. Cuando COPY_SUBFOLDERS no se establece para una operación de copia, solo se copia la carpeta identificada por _lpEntryID._ Con una operación de movimiento, el comportamiento COPY_SUBFOLDERS es el predeterminado independientemente de si se establece la marca. 
    
FOLDER_DIALOG 
  
> Solicita la presentación de un indicador de progreso.
    
FOLDER_MOVE 
  
> La carpeta debe moverse en lugar de copiarse. Si FOLDER_MOVE no está establecido, se copia la carpeta.
    
MAPI_UNICODE 
  
> El nombre de la carpeta está en formato Unicode. Si no MAPI_UNICODE marca, el nombre de la carpeta está en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta se ha copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta de la carpeta de destino. El proveedor del almacén de mensajes requiere que los nombres de carpeta sean únicos. La operación se detiene sin completarse.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todas las entradas se copiaron correctamente. Cuando se devuelve esta advertencia, la llamada debe controlarse como correcta. Para probar esta advertencia, use la **HR_FAILED** macro. Para obtener más información, vea [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::CopyFolder** se implementa para objetos de soporte del proveedor del almacén de mensajes. Los proveedores de almacén de mensajes pueden llamar a **IMAPISupport::CopyFolder en** su implementación de [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) para copiar o mover una sola carpeta de una carpeta primaria a otra. 
  
 **IMAPISupport::CopyFolder** agrega la carpeta copiada o movida como subcarpeta de la carpeta de destino. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **IMAPISupport::CopyFolder** permite cambiar el nombre y el movimiento simultáneos de carpetas y copiar o mover subcarpetas de la carpeta afectada. Para copiar o mover todas las subcarpetas anidadas en la carpeta copiada o movida, pase la marca COPY_SUBFOLDERS en  _ulFlags_. 
  
Espere los siguientes valores devueltos en las siguientes condiciones:
  
|**Condition**|**Valor devuelto**|
|:-----|:-----|
|**CopyFolder** copió o movió correctamente la carpeta y todas sus subcarpetas, si procede.  <br/> |S_OK  <br/> |
|**CopyFolder** no pudo copiar o mover correctamente todas las carpetas.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** no se pudo completar.  <br/> |Cualquier valor de error  <br/> |
   
Si **CopyFolder** devuelve un valor de error, no continúe con la suposición de que no se ha realizado ningún trabajo. Una o más carpetas podrían haber sido copiadas o movida antes de **que CopyFolder** experimentara el error. 
  
## <a name="see-also"></a>Vea también



[IMAPISupport: IUnknown](imapisupportiunknown.md)

