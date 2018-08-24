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
ms.openlocfilehash: bf6386ae3a7d835c8748e332235d8737c7a502e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589472"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Se abre un contenedor, usuario o lista de distribución, de mensajería y devuelve un puntero a una implementación de interfaz para proporcionar más acceso.
  
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
  
> [entrada] Un puntero al identificador de entrada del contenedor, usuario o lista de distribución para abrir de mensajería.
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto abierto. Pasando NULL, devuelve el identificador de la interfaz del objeto estándar. Para contenedores, es la interfaz estándar de [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). El estándar de interfaces de objetos de la libreta de direcciones son [IDistList: IMAPIContainer](idistlistimapicontainer.md) para obtener una lista de distribución y [IMailUser: IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto. Se pueden establecer los siguientes indicadores:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abran con los permisos de red máximo permitidos para el acceso de usuarios y el número máximo de clientes aplicación. Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se debe abrir el objeto con permisos de lectura y escritura; Si el cliente no tiene permiso de sólo lectura, se debe abrir el objeto con permiso de sólo lectura.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que el método **OpenEntry** correctamente, devolver, posiblemente, antes de que el cliente de la llamada totalmente tener acceso a los objetos. Si no se tiene acceso al objeto, realizar una llamada de objeto posteriores puede provocar un error. 
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren con acceso de solo lectura y clientes no deben asumir que se ha concedido permiso de lectura y escritura.
    
 _lpulObjType_
  
> [out] Un puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> [out] Un puntero a un puntero al objeto abierto.
    
## <a name="remarks"></a>Comentarios

S_OK 
  
> El objeto se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Puede que el usuario no tiene permisos suficientes para abrir el objeto o se ha intentado abrir un objeto de sólo lectura con permiso de lectura y escritura.
    
MAPI_E_NOT_FOUND 
  
> El identificador de entrada especificado por _lpEntryID_ no representan un objeto. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada en el parámetro _lpEntryID_ no es un formato reconocido por el proveedor de la libreta de direcciones. 
    
## <a name="remarks"></a>Comentarios

MAPI llama al método de **OpenEntry** para abrir un contenedor, usuario o lista de distribución de mensajería. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Antes de MAPI llama a su método **OpenEntry** , determina que el identificador de entrada en el parámetro _lpEntryID_ pertenece a usted y no a otro proveedor. Para ello, MAPI que coincidan con la estructura [MAPIUID](mapiuid.md) en el identificador de entrada con el **MAPIUID** que se ha registrado llamando al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) en el inicio. 
  
Abra el objeto como de solo lectura, a menos que se establece la marca MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags indicado_ . Si no permite la modificación para el objeto solicitado, no abra el objeto en absoluto y devolver MAPI_E_NO_ACCESS. 
  
Si MAPI pasa NULL para _lpEntryID_, abra el contenedor raíz en la jerarquía del contenedor.
  
El objeto que se le pide para abrir podría ser un objeto copiado de otro proveedor. En este caso, admitirá la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si el objeto es compatible con esta propiedad, llame al método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para enlazar al código para esta entrada en el proveedor extranjero, pasando **PR_TEMPLATEID** en el parámetro _lpTemplateID_ y 0 en la ulTemplateFlags _ _parámetro. **IMAPISupport::OpenTemplateID** pasa esta información al proveedor de externa en una llamada al método [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) del proveedor externo. Si **IMAPISupport::OpenTemplateID** genera un error, suele ser debido a que el proveedor externo no está disponible o no está incluido en el perfil, intente continuar por el tratamiento de la entrada independiente como de solo lectura. Para obtener más información acerca de cómo abrir entradas de la libreta de direcciones externa, vea [actuar como un proveedor de libreta de direcciones de Host](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Vea también



[IABLogon : IUnknown](iablogoniunknown.md)

