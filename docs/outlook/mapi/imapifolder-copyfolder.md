---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 134a492dbc86dd0ce6b3795d5ae40b334c14d468
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585153"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve una subcarpeta.
  
```cpp
HRESULT CopyFolder(
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

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada de la subcarpeta para copiar o mover.
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta que señala el parámetro _lpDestFolder_ . Pasando NULL hace que el proveedor de servicios devolver la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Los valores válidos para _lpInterface_ son IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer y IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [entrada] Un puntero a la carpeta abierta para recibir la subcarpeta copiada o movida.
    
 _lpszNewFolderName_
  
> [entrada] Un puntero en el nombre de la carpeta que se ha movido o copiado en su nuevo destino. Si _lpszNewFolderName_ se establece en NULL, se usa el nombre de la subcarpeta de origen para el nombre de la carpeta de destino. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. El parámetro _ulUIParam_ se omite a menos que se establece la marca FOLDER_DIALOG en el parámetro _ulFlags indicado_ . 
    
 _lpProgress_
  
> [entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI. El parámetro _lpProgress_ se omite a menos que se establece la marca FOLDER_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
COPY_SUBFOLDERS 
  
> También se deben copiar todas las subcarpetas en la subcarpeta que se va a copiar. Cuando COPY_SUBFOLDERS no está establecido para una operación de copia, se copia sólo la subcarpeta identificada por _lpEntryID_ . Con una operación de movimiento, el comportamiento COPY_SUBFOLDERS es el valor predeterminado, independientemente de si se establece la marca. 
    
FOLDER_DIALOG 
  
> Solicita la visualización de un indicador de progreso.
    
FOLDER_MOVE 
  
> La subcarpeta es va a mover en lugar de copiado. Si no se establece FOLDER_MOVE, se copia la subcarpeta.
    
MAPI_DECLINE_OK 
  
> El proveedor de almacenamiento de mensaje le informa de que si implementa **CopyFolder** mediante una llamada al método [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) o [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) del objeto de su soporte técnico, **CopyFolder** debe devolver en su lugar inmediatamente MAPI_E_ DECLINE_COPY. 
    
MAPI_UNICODE. 
  
> El nombre de la carpeta de destino está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., el nombre de la carpeta está en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta especificada se ha copiado o movido correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y el proveedor de almacén de mensajes no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y el proveedor de almacenamiento de mensaje admite sólo Unicode.
    
MAPI_E_COLLISION 
  
> El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta en la carpeta de destino. El proveedor de almacén de mensajes requiere nombres de carpeta única.
    
MAPI_E_DECLINE_COPY 
  
> El proveedor implementa este método mediante una llamada a un método del objeto de soporte, y el autor de la llamada ha pasado la marca MAPI_DECLINE_OK.
    
MAPI_E_FOLDER_CYCLE 
  
> La carpeta de origen, directa o indirectamente contiene la carpeta de destino. Trabajo significativo es posible que se han realizado antes de que se ha detectado esta condición, por lo que se puede modificar parcialmente la carpeta de origen y de destino. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todas las entradas se copiaron correctamente. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder::CopyFolder** copia o mueve una subcarpeta de una ubicación a otra. La subcarpeta se copien o muevan se agrega a la carpeta de destino como una subcarpeta. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Cuando la operación de copiar o mover implica más de una carpeta, como se indica mediante la configuración de la marca COPY_SUBFOLDERS, realizar la operación más completo posible para cada carpeta. En ocasiones, una de las carpetas que se va a mover o copiar no existe o ya se ha movido o copiado en otro lugar. No detiene la operación de forma prematura a menos que se produzca un error que está fuera de su control, como la falta de memoria, está quedando sin espacio en disco o daños en el almacén de mensajes.
  
Intente conservar todos los identificadores de entrada del mensaje en los mensajes copiados. También debe intentar conservar los identificadores de entrada, pero no es necesario. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espera a que estos valores devueltos en las siguientes condiciones.
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**CopyFolder** correctamente haya copiado o movido todos los mensajes y subcarpeta.  <br/> |S_OK  <br/> |
|**CopyFolder** no pudo copiar o mover todos los mensajes y subcarpeta correctamente.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** no pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando no se puede completar **CopyFolder** , no asuma que se ha realizado ningún trabajo. Es posible que han sido **CopyFolder** capaz de copiar o mover uno o varios de los mensajes y subcarpetas antes de encontrar el error. 
  
Si se pasa un identificador de entrada para una carpeta que no existe en _lpEntryID_, **CopyFolder** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, según la implementación del almacén de mensajes. 
  
Dependiendo del proveedor de almacén de mensajes, el identificador de entrada del mensaje original puede o no es posible que se conserva en el mensaje copiado. Debe conservar los identificadores de entrada siempre que sea posible, pero no es un requisito. Por lo general puede confiar en los siguientes escenarios:
  
- Al mover una carpeta entre dos tipos diferentes de los almacenes de mensajes, se garantiza que el identificador de entrada cambia.
    
- Al mover una carpeta entre dos almacenes de mensajes del mismo tipo, casi siempre se cambia el identificador de entrada.
    
- Cuando se mueve una carpeta a otra ubicación en el mismo almacén de mensajes, el identificador de entrada puede o puede que no cambie, según el mensaje de proveedor de almacén.
    
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI usa el método **IMAPIFolder::CopyFolder** para copiar las carpetas desde una ubicación a otra. MFCMAPI recuerda la carpeta de origen durante la operación de copia y realmente realiza la copia durante la operación de pegado.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

