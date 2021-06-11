---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423639"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un objeto en el contenedor y devuelve un puntero de interfaz para obtener más acceso.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada del objeto que se debe abrir. Si  _lpEntryID_ se establece en NULL, se abrirá el contenedor de nivel superior de la jerarquía del contenedor. 
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para obtener acceso al objeto. Si se pasa NULL, se devuelve el identificador de la interfaz estándar del objeto. Para los mensajes, la interfaz estándar [es IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); para carpetas, es [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Las interfaces estándar para objetos de libreta de direcciones son [IDistList : IMAPIContainer](idistlistimapicontainer.md) para una lista de distribución e [IMailUser : IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre el objeto. Se pueden establecer las siguientes marcas:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abra con los permisos máximos de red permitidos para el usuario y el acceso máximo a la aplicación cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con permiso de lectura y escritura; si el cliente tiene acceso de solo lectura, el objeto debe abrirse con acceso de solo lectura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que OpenEntry** vuelva correctamente, posiblemente antes de que el objeto esté totalmente disponible para el cliente que realiza la llamada. Si el objeto no está disponible, realizar una llamada de objeto posterior puede generar un error. 
    
MAPI_MODIFY 
  
> Solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren con acceso de solo lectura y los clientes no deben trabajar con la suposición de que se ha concedido permiso de lectura y escritura. 
    
SHOW_SOFT_DELETES
  
> Muestra los elementos marcados actualmente como eliminados temporalmente; es decir, se encuentran en la fase de tiempo de retención de elementos eliminados.
    
 _lpulObjType_
  
> [salida] Puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> [salida] Puntero a un puntero a la implementación de la interfaz que se usará para obtener acceso al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> El usuario no tiene permisos suficientes para abrir el objeto o se intentó abrir un objeto de solo lectura con permiso de lectura y escritura.
    
MAPI_E_NOT_FOUND 
  
> El identificador de entrada especificado por  _lpEntryID_ no representa un objeto. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada en el  _parámetro lpEntryID_ no es de un formato reconocido por el contenedor. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPIContainer::OpenEntry** abre un objeto en todo un contenedor y devuelve un puntero a una implementación de interfaz para usarlo para obtener más acceso. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Dado que los proveedores de servicios no son necesarios para devolver una implementación de interfaz del tipo especificado por el identificador de interfaz en el parámetro _lpInterface,_ compruebe el valor señalado por el parámetro _lpulObjType._ Si es necesario, convierte el puntero devuelto en  _lppUnk_ a un puntero del tipo adecuado. 
  
De forma predeterminada, los proveedores de servicios abren objetos con acceso de solo lectura a menos que establezca la marca MAPI_MODIFY o MAPI_BEST_ACCESS. Cuando se establece una de estas marcas, los proveedores de servicios intentan devolver un objeto modificable. Sin embargo, no suponga que, dado que solicitó un objeto modificable, el objeto abierto tiene permiso de lectura y escritura. Planee la posibilidad de que se producirá un  error en una modificación posterior o recupere la propiedad PR_ACCESS_LEVEL del objeto para determinar el nivel de acceso concedido **por OpenEntry**.
  
## <a name="see-also"></a>Vea también



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

