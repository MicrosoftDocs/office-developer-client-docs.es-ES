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
ms.openlocfilehash: c13ab9ce9c2564c39bfe9b2689f05439bc7b74ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817199"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**Hace referencia a**: Outlook 
  
Abre un objeto en el contenedor, la devolución de un puntero de interfaz para aún más el acceso.
  
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

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del objeto que se va a abrir. Si _lpEntryID_ se establece en NULL, se abre el contenedor de nivel superior en la jerarquía del contenedor. 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto. Si se pasa NULL da como resultado el identificador de la interfaz del objeto estándar que se devuelven. Para los mensajes, es la interfaz estándar de [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); para las carpetas, es [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). El estándar de interfaces de objetos de la libreta de direcciones son [IDistList: IMAPIContainer](idistlistimapicontainer.md) para obtener una lista de distribución y [IMailUser: IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto. Se pueden establecer los siguientes indicadores:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abrirá con los permisos de red máximo permitidos para el acceso de usuarios y el número máximo de clientes aplicación. Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se debe abrir el objeto con permisos de lectura y escritura; Si el cliente no tiene acceso de solo lectura, el objeto se debe abrir con acceso de solo lectura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenEntry** devolver de correctamente, posiblemente antes de que el objeto está totalmente disponible para el cliente de la llamada. Si el objeto no está disponible, realizar una llamada de objeto posteriores puede provocar un error. 
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren con acceso de solo lectura y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
SHOW_SOFT_DELETES
  
> Muestra los elementos que actualmente están marcados como suaves eliminan, es decir, se encuentran en la retención de elementos eliminados fase de tiempo.
    
 _lpulObjType_
  
> [out] Un puntero al tipo de objeto abierto.
    
 _lppUnk_
  
> [out] Un puntero a un puntero a la implementación de la interfaz a usar para tener acceso al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> El usuario no tiene permisos suficientes para abrir el objeto o se ha intentado abrir un objeto de sólo lectura con permiso de lectura y escritura.
    
MAPI_E_NOT_FOUND 
  
> El identificador de entrada especificado por _lpEntryID_ no representan un objeto. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada en el parámetro _lpEntryID_ no es un formato reconocido por el contenedor. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPIContainer::OpenEntry** abre un objeto a lo largo de un contenedor y devuelve un puntero a una implementación de interfaz que se usará para aún más el acceso. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Dado que los proveedores de servicios no son necesarios para devolver una implementación de interfaz del tipo especificado por el identificador de interfaz en el parámetro _lpInterface_ , comprobar el valor al que señala el parámetro _lpulObjType_ . Si es necesario, convertir el puntero devuelto en _lppUnk_ a un puntero del tipo apropiado. 
  
De forma predeterminada, los proveedores de servicios abran objetos con acceso de sólo lectura a menos que establezca marca la MAPI_MODIFY o MAPI_BEST_ACCESS. Cuando se establece una de estas marcas, proveedores de servicios intentan devolver un objeto modificable. Sin embargo, no asuma que debido a que se solicitó un objeto modificable que el objeto abierto tiene permiso de lectura y escritura. Ya sea, la planeación de la posibilidad de que una modificación posterior para producir un error o recuperar la propiedad del objeto **PR_ACCESS_LEVEL** determinar el nivel de acceso concedido por **OpenEntry**.
  
## <a name="see-also"></a>Vea también



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

