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
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280181"
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

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada de la subcarpeta que se va a copiar o mover.
    
 _lpInterface_
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la carpeta a la que apunta el parámetro _lpDestFolder_ . Si se pasa NULL, el proveedor de servicios devuelve la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Los valores válidos para _lpInterface_ incluyen IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer y IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> a Un puntero a la carpeta abierta para recibir la subcarpeta copiada o movida.
    
 _lpszNewFolderName_
  
> a Un puntero al nombre de la carpeta copiada o movida en su nuevo destino. Si _lpszNewFolderName_ se establece en null, se usa el nombre de la subcarpeta de origen para el nombre de la carpeta de destino. 
    
 _ulUIParam_
  
> a Identificador de la ventana primaria del indicador de progreso. El parámetro _ulUIParam_ se omite a menos que se establezca la marca FOLDER_DIALOG en el parámetro _ulFlags_ . 
    
 _lpProgress_
  
> a Un puntero a un objeto Progress que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca FOLDER_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
COPY_SUBFOLDERS 
  
> También se deben copiar todas las subcarpetas de la subcarpeta que se va a copiar. Cuando COPY_SUBFOLDERS no se establece para una operación de copia, solo se copia la subcarpeta identificada por _lpEntryID_ . Con una operación de movimiento, el comportamiento de COPY_SUBFOLDERS es el valor predeterminado independientemente de si se ha establecido la marca. 
    
FOLDER_DIALOG 
  
> Solicita la presentación de un indicador de progreso.
    
FOLDER_MOVE 
  
> La subcarpeta se moverá en lugar de copiarse. Si no se establece FOLDER_MOVE, se copia la subcarpeta.
    
MAPI_DECLINE_OK 
  
> Informa al proveedor de almacenamiento de mensajes que si implementa **CopyFolder** mediante una llamada al método [IMAPISupport::D ocopyto](imapisupport-docopyto.md) o [IMAPISupport::D Ocopyprops](imapisupport-docopyprops.md) del objeto support, **CopyFolder** debe devolver MAPI_E_ en su lugar. DECLINE_COPY. 
    
MAPI_UNICODE 
  
> El nombre de la carpeta de destino está en formato Unicode. Si no se establece la marca MAPI_UNICODE, el nombre de la carpeta está en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta especificada se ha copiado o movido correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y el proveedor de almacenamiento de mensajes no admite Unicode, o no se estableció MAPI_UNICODE y el proveedor de almacenamiento de mensajes solo admite Unicode.
    
MAPI_E_COLLISION 
  
> El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta de la carpeta de destino. El proveedor de almacenamiento de mensajes requiere nombres de carpeta únicos.
    
MAPI_E_DECLINE_COPY 
  
> El proveedor implementa este método llamando a un método de objeto de soporte y el autor de la llamada ha pasado la marca MAPI_DECLINE_OK.
    
MAPI_E_FOLDER_CYCLE 
  
> La carpeta de origen contiene directa o indirectamente la carpeta de destino. Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que la carpeta de origen y de destino se puede modificar parcialmente. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se realizó correctamente, pero no todas las entradas se copiaron correctamente. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder:: CopyFolder** copia o mueve una subcarpeta de una ubicación a otra. La subcarpeta que se va a copiar o mover se agrega a la carpeta de destino como una subcarpeta. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando la operación de copia o movimiento implica más de una carpeta, como se indica mediante la configuración de la marca COPY_SUBFOLDERS, realice la operación lo más completamente posible para cada carpeta. A veces, una de las carpetas que se van a mover o copiar no existe o ya se ha movido o copiado en otra ubicación. No detenga la operación prematuramente a menos que se produzca un error que esté más allá del control, como la falta de memoria, la falta de espacio en disco o que esté dañada en el almacén de mensajes.
  
Intente conservar todos los identificadores de entrada de mensaje en los mensajes copiados. También debe intentar conservar los identificadores de entrada, pero no es necesario. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espere estos valores devueltos en las siguientes condiciones.
  
|**Condition**|**Valor devuelto**|
|:-----|:-----|
|**CopyFolder** ha copiado o movido correctamente todos los mensajes y subcarpetas.  <br/> |S_OK  <br/> |
|**CopyFolder** no pudo copiar o mover correctamente todos los mensajes y subcarpetas.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** no se pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando **CopyFolder** no pueda completarse, no dé por supuesto que no se ha realizado ningún trabajo. Es posible que **CopyFolder** haya podido copiar o mover uno o más de los mensajes y subcarpetas antes de que se produzca el error. 
  
Si se pasa un identificador de entrada para una carpeta que no existe en _lpEntryID_, **CopyFolder** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, en función de la implementación del almacén de mensajes. 
  
Según el proveedor de almacenamiento de mensajes, el identificador de entrada del mensaje original puede o no conservarse en el mensaje copiado. Debe conservar los identificadores de entrada siempre que sea posible, pero no es un requisito. Por lo general, puede depender de los siguientes escenarios:
  
- Cuando se mueve una carpeta entre dos tipos diferentes de almacenes de mensajes, se garantiza que el identificador de entrada cambiará.
    
- Cuando se mueve una carpeta entre dos almacenes de mensajes del mismo tipo, el identificador de entrada casi siempre cambia.
    
- Cuando mueve una carpeta a otra ubicación en el mismo almacén de mensajes, el identificador de entrada puede o no cambiar según el proveedor de almacenamiento de mensajes.
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnPasteFolder  <br/> |MFCMAPI usa el método **IMAPIFolder:: CopyFolder** para copiar carpetas de una ubicación a otra. MFCMAPI recuerda la carpeta de origen durante la operación de copia y, en realidad, realiza la copia durante la operación de pegado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

