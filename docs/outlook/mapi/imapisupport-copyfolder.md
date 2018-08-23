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
ms.openlocfilehash: 6ffbf74496d4b61357a0fb473b82deedf39ee576
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570677"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve una carpeta de su carpeta primaria actual a otra carpeta primaria.
  
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
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta principal de la carpeta que desea copiar o mover.
    
 _lpSrcFolder_
  
> [entrada] Un puntero a la carpeta principal de la carpeta que desea copiar o mover. 
    
 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada que señala _lpEntryID_.
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada de la carpeta que desea copiar o mover. 
    
 _lpInterface_
  
> [entrada] Reservado; debe ser NULL.
    
 _lpDestFolder_
  
> [entrada] Un puntero a la carpeta que va a recibir la carpeta para ser copiado o movido.
    
 _lpszNewFolderName_
  
> [entrada] Un puntero en el nombre de la carpeta que se ha movido o copiado; de lo contrario, NULL, que indica que la carpeta que se ha movido o copiada debe tener el mismo nombre que la carpeta de origen (es decir, la carpeta indicada por _lpEntryID_).
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana para el cuadro de diálogo de indicador de progreso y ventanas relacionadas. El parámetro _ulUIParam_ se omite a menos que se establece la marca FOLDER_DIALOG en el parámetro _ulFlags indicado_ . 
    
 _lpProgress_
  
> [entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI. El parámetro _lpProgress_ se omite a menos que se establece la marca FOLDER_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se lleva a cabo la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
COPY_SUBFOLDERS 
  
> Todas las subcarpetas de la carpeta deben ser copiado o movido. Cuando COPY_SUBFOLDERS no está establecido para una operación de copia, se copia sólo la carpeta identificada por _lpEntryID_ . Con una operación de movimiento, el comportamiento COPY_SUBFOLDERS es el valor predeterminado, independientemente de si se establece la marca. 
    
FOLDER_DIALOG 
  
> Solicita la visualización de un indicador de progreso.
    
FOLDER_MOVE 
  
> La carpeta se va a mover en lugar de copiado. Si no se establece FOLDER_MOVE, se copia la carpeta.
    
MAPI_UNICODE. 
  
> El nombre de la carpeta está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., el nombre de la carpeta está en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta se ha copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta en la carpeta de destino. El proveedor de almacén de mensajes requiere que los nombres de carpeta ser únicos. Detiene la operación sin completar.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todas las entradas se copiaron correctamente. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::CopyFolder** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes. Los proveedores de almacén de mensajes pueden llamar a **IMAPISupport::CopyFolder** en su implementación de [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) para copiar o mover una sola carpeta desde la carpeta principal de uno a otro. 
  
 **IMAPISupport::CopyFolder** agrega la carpeta que se ha movido o copiada como una subcarpeta de la carpeta de destino. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **IMAPISupport::CopyFolder** permite cambiar el nombre y mover de carpetas y la copia o traslado de las subcarpetas de la carpeta afectada simultáneas. Para copiar o mover todas las subcarpetas anidadas en la carpeta que se ha movido o copiada, pase el indicador COPY_SUBFOLDERS _ulFlags_. 
  
Esperar que el siguiente devolver valores en las siguientes condiciones:
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**CopyFolder** correctamente copiado o había movido la carpeta y todas sus subcarpetas, si procede.  <br/> |S_OK  <br/> |
|**CopyFolder** no pudo copiar o mover todas las carpetas correctamente.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** no pudo completar.  <br/> |Cualquier valor de error  <br/> |
   
Si **CopyFolder** devuelve un valor de error, no continúe en la suposición de que se ha realizado ningún trabajo. Una o varias carpetas podrían se han copiado o movido antes de **CopyFolder** tuvo el error. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPISupport: IUnknown](imapisupportiunknown.md)

