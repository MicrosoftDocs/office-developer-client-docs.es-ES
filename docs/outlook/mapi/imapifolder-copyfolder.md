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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425662"
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
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada de la subcarpeta que se debe copiar o mover.
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para obtener acceso a la carpeta a la que apunta el parámetro _lpDestFolder._ Si se pasa NULL, el proveedor de servicios devuelve la interfaz de carpeta estándar, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Los valores válidos para  _lpInterface_ incluyen IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer y IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Puntero a la carpeta abierta para recibir la subcarpeta copiada o movida.
    
 _lpszNewFolderName_
  
> [in] Puntero al nombre de la carpeta copiada o movida en su nuevo destino. Si  _lpszNewFolderName_ se establece en NULL, se usa el nombre de la subcarpeta de origen para el nombre de la carpeta de destino. 
    
 _ulUIParam_
  
> [in] Identificador de la ventana principal del indicador de progreso. El _parámetro ulUIParam_ se omite a menos que FOLDER_DIALOG marca del parámetro _ulFlags._ 
    
 _lpProgress_
  
> [in] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI. El  _parámetro lpProgress_ se omite a menos que FOLDER_DIALOG marca se establezca en  _ulFlags_.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla la operación de copiar o mover. Se pueden establecer las siguientes marcas:
    
COPY_SUBFOLDERS 
  
> Todas las subcarpetas de la subcarpeta que se van a copiar también deben copiarse. Cuando COPY_SUBFOLDERS no se establece para una operación de copia, solo se copia la subcarpeta identificada por _lpEntryID._ Con una operación de movimiento, el comportamiento COPY_SUBFOLDERS es el predeterminado independientemente de si se establece la marca. 
    
FOLDER_DIALOG 
  
> Solicita la presentación de un indicador de progreso.
    
FOLDER_MOVE 
  
> La subcarpeta se debe mover en lugar de copiarse. Si FOLDER_MOVE se establece, se copia la subcarpeta.
    
MAPI_DECLINE_OK 
  
> Informa al proveedor del almacén de mensajes de que si implementa **CopyFolder** llamando al método [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) o [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) del objeto de soporte técnico, **CopyFolder** debería devolver inmediatamente MAPI_E_DECLINE_COPY. 
    
MAPI_UNICODE 
  
> El nombre de la carpeta de destino está en formato Unicode. Si la MAPI_UNICODE no está establecida, el nombre de la carpeta está en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta especificada se ha copiado o movido correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y el proveedor del almacén de mensajes no admite Unicode o MAPI_UNICODE no se estableció y el proveedor del almacén de mensajes solo admite Unicode.
    
MAPI_E_COLLISION 
  
> El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta de la carpeta de destino. El proveedor del almacén de mensajes requiere nombres de carpeta únicos.
    
MAPI_E_DECLINE_COPY 
  
> El proveedor implementa este método llamando a un método de objeto de soporte técnico y el autor de la llamada ha pasado la marca MAPI_DECLINE_OK.
    
MAPI_E_FOLDER_CYCLE 
  
> La carpeta de origen contiene directa o indirectamente la carpeta de destino. Es posible que se haya realizado un trabajo significativo antes de detectar esta condición, por lo que la carpeta de origen y de destino puede modificarse parcialmente. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todas las entradas se copiaron correctamente. Cuando se devuelve esta advertencia, la llamada debe controlarse como correcta. Para probar esta advertencia, use la **HR_FAILED** macro. Para obtener más información, vea [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El **método IMAPIFolder::CopyFolder** copia o mueve una subcarpeta de una ubicación a otra. La subcarpeta que se copia o mueve se agrega a la carpeta de destino como subcarpeta. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando la operación de copiar o mover implica más de una carpeta, como se indica estableciendo la marca COPY_SUBFOLDERS, realice la operación de la forma más completa posible para cada carpeta. A veces, una de las carpetas que se va a mover o copiar no existe o ya se ha movido o copiado en otro lugar. No detenga la operación prematuramente a menos que se produzca un error que esté fuera de su control, como que se esté quedando sin memoria, que se esté quedando sin espacio en disco o que se produzcan daños en el almacén de mensajes.
  
Intente conservar todos los identificadores de entrada de mensajes en los mensajes copiados. También debe intentar conservar los identificadores de entrada, pero no es necesario. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espere estos valores devueltos en las siguientes condiciones.
  
|**Condition**|**Valor devuelto**|
|:-----|:-----|
|**CopyFolder** ha copiado o movido correctamente todos los mensajes y subcarpetas.  <br/> |S_OK  <br/> |
|**CopyFolder** no pudo copiar o mover correctamente todos los mensajes y subcarpetas.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** no se pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando **CopyFolder** no se pueda completar, no suponga que no se ha realizado ningún trabajo. Es posible que **CopyFolder** haya podido copiar o mover uno o varios de los mensajes y subcarpetas antes de encontrar el error. 
  
Si se pasa un identificador de entrada de una carpeta que no existe en  _lpEntryID_, **CopyFolder** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, según la implementación del almacén de mensajes. 
  
Según el proveedor del almacén de mensajes, el identificador de entrada del mensaje original puede o no conservarse en el mensaje copiado. Debe conservar los identificadores de entrada siempre que sea posible, pero no es un requisito. Por lo general, puede depender de los siguientes escenarios:
  
- Al mover una carpeta entre dos tipos diferentes de almacenes de mensajes, se garantiza que el identificador de entrada cambie.
    
- Al mover una carpeta entre dos almacenes de mensajes del mismo tipo, el identificador de entrada casi siempre cambia.
    
- Al mover una carpeta a otra ubicación del mismo almacén de mensajes, el identificador de entrada puede o no cambiar, según el proveedor del almacén de mensajes.
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI usa el **método IMAPIFolder::CopyFolder** para copiar carpetas de una ubicación a otra. MFCMAPI recuerda la carpeta de origen durante la operación de copia y, en realidad, realiza la copia durante la operación de pegado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

