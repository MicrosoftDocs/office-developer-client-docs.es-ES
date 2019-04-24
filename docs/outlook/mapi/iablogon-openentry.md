---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348940"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un contenedor, un usuario de mensajería o una lista de distribución y devuelve un puntero a una implementación de interfaz para proporcionar más acceso.
  
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
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada del contenedor, el usuario de mensajería o la lista de distribución que se va a abrir.
    
 _lpInterface_
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a utilizar para tener acceso al objeto Open. Si se pasa NULL, se devuelve el identificador de la interfaz estándar del objeto. Para los contenedores, la interfaz estándar es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Las interfaces estándar para los objetos de la libreta de direcciones son [IDistList: IMAPIContainer](idistlistimapicontainer.md) para una lista de distribución y [IMailUser: IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre el objeto. Se pueden establecer los siguientes indicadores:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abra con los permisos de red máximos permitidos para el usuario y el acceso máximo a la aplicación cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con permiso de lectura y escritura; Si el cliente tiene permiso de solo lectura, el objeto debe abrirse con permiso de solo lectura.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que el método **OpenEntry** se devuelva correctamente, posiblemente antes de que el cliente de la llamada haya tenido acceso total al objeto. Si no se tiene acceso al objeto, realizar una llamada subsiguiente a un objeto puede generar un error. 
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. De forma predeterminada, los objetos se abren con acceso de solo lectura y los clientes no deben asumir que se ha concedido el permiso de lectura y escritura.
    
 _lpulObjType_
  
> contempla Un puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> contempla Un puntero a un puntero al objeto abierto.
    
## <a name="remarks"></a>Comentarios

S_OK 
  
> El objeto se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Puede que el usuario no tenga permisos suficientes para abrir el objeto o que se haya intentado abrir un objeto de solo lectura con permiso de lectura y escritura.
    
MAPI_E_NOT_FOUND 
  
> El identificador de entrada especificado por _lpEntryID_ no representa un objeto. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada en el parámetro _lpEntryID_ no tiene un formato reconocido por el proveedor de la libreta de direcciones. 
    
## <a name="remarks"></a>Comentarios

MAPI llama al método **OpenEntry** para abrir un contenedor, un usuario de mensajería o una lista de distribución. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Antes de que MAPI llame a su método **OpenEntry** , determina que el identificador de entrada en el parámetro _lpEntryID_ le pertenece y no a otro proveedor. MAPI hace esto haciendo coincidir la estructura [MAPIUID](mapiuid.md) del identificador de entrada con el **MAPIUID** que ha registrado llamando al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) al iniciar. 
  
Abra el objeto como de solo lectura, a menos que el marcador MAPI_MODIFY o MAPI_BEST_ACCESS esté establecido en el parámetro _ulFlags_ . Si no permite la modificación del objeto solicitado, no abra el objeto en absoluto y devuelva MAPI_E_NO_ACCESS. 
  
Si MAPI pasa NULL para _lpEntryID_, abra el contenedor raíz en la jerarquía de contenedores.
  
El objeto que se le solicita que abra puede ser un objeto copiado de otro proveedor. En este caso, será compatible con la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si el objeto admite esta propiedad, llame al método [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) para enlazar con el código de esta entrada en el proveedor externo, pasando **PR_TEMPLATEID** en el parámetro _LpTemplateID_ y 0 en el _ulTemplateFlags _parámetro. **IMAPISupport:: OpenTemplateID** pasa esta información al proveedor externo en una llamada al método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) del proveedor externo. Si **IMAPISupport:: OpenTemplateID** genera un error, normalmente porque el proveedor externo no está disponible o no está incluido en el perfil, intente continuar tratando la entrada independiente como de solo lectura. Para obtener más información acerca de cómo abrir entradas de la libreta de direcciones externa, consulte [actuar como proveedor de la libreta de direcciones de host](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Vea también



[IABLogon : IUnknown](iablogoniunknown.md)

