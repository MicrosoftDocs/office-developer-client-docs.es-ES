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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409233"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un contenedor, un usuario de mensajería o una lista de distribución y devuelve un puntero a una implementación de interfaz para proporcionar acceso adicional.
  
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
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada del contenedor, usuario de mensajería o lista de distribución que se abrirá.
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para tener acceso al objeto abierto. Si se pasa NULL, se devuelve el identificador de la interfaz estándar del objeto. Para contenedores, la interfaz estándar [es IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Las interfaces estándar para objetos de libreta de direcciones son [IDistList: IMAPIContainer](idistlistimapicontainer.md) para una lista de distribución e [IMailUser : IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se abre el objeto. Se pueden establecer las siguientes marcas:
    
MAPI_BEST_ACCESS 
  
> Solicita que el objeto se abra con los permisos de red máximos permitidos para el usuario y el acceso máximo a la aplicación cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con permiso de lectura y escritura; si el cliente tiene permiso de solo lectura, el objeto debe abrirse con permiso de solo lectura.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **el método OpenEntry** vuelva correctamente, posiblemente antes de que el cliente de llamada tenga acceso al objeto por completo. Si no se tiene acceso al objeto, realizar una llamada a objeto posterior puede generar un error. 
    
MAPI_MODIFY 
  
> Solicita permiso de lectura y escritura. De forma predeterminada, los objetos se abren con acceso de solo lectura y los clientes no deben suponer que se ha concedido permiso de lectura y escritura.
    
 _lpulObjType_
  
> [salida] Puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> [salida] Puntero a un puntero al objeto abierto.
    
## <a name="remarks"></a>Comentarios

S_OK 
  
> El objeto se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> El usuario no tiene permisos suficientes para abrir el objeto o se intentó abrir un objeto de solo lectura con permiso de lectura y escritura.
    
MAPI_E_NOT_FOUND 
  
> El identificador de entrada especificado  _por lpEntryID_ no representa un objeto. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El identificador de entrada en  _el parámetro lpEntryID_ no tiene un formato reconocido por el proveedor de libreta de direcciones. 
    
## <a name="remarks"></a>Comentarios

MAPI llama al **método OpenEntry** para abrir un contenedor, un usuario de mensajería o una lista de distribución. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Antes de que MAPI llame **al método OpenEntry,** determina que el identificador de entrada del parámetro  _lpEntryID_ pertenece a usted y no a otro proveedor. MAPI hace esto al hacer coincidir la estructura [MAPIUID](mapiuid.md) en el identificador de entrada con el **MAPIUID** que registró llamando al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) en el inicio. 
  
Abra el objeto como de solo lectura, a menos MAPI_MODIFY o MAPI_BEST_ACCESS marca esté establecida en el _parámetro ulFlags._ Si no permite la modificación del objeto solicitado, no abra el objeto en absoluto y devuelva MAPI_E_NO_ACCESS. 
  
Si MAPI pasa NULL para  _lpEntryID,_ abra el contenedor raíz en la jerarquía de contenedores.
  
El objeto que se le pide que abra puede ser un objeto copiado de otro proveedor. En este caso, admitirá la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si el objeto admite esta propiedad, llame al método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para enlazar al código de esta entrada en el proveedor externo, pasando **PR_TEMPLATEID** en el parámetro _lpTemplateID_ y 0 en el parámetro _ulTemplateFlags._ **IMAPISupport::OpenTemplateID** pasa esta información al proveedor externo en una llamada al método [IABLogon::OpenTemplateID del](iablogon-opentemplateid.md) proveedor externo. Si **IMAPISupport::OpenTemplateID** genera un error, normalmente porque el proveedor externo no está disponible o no está incluido en el perfil, intente continuar tratando la entrada independiente como de solo lectura. Para obtener más información acerca de cómo abrir entradas de libretas de direcciones externa, vea [Actuar como proveedor de libretas de direcciones host.](acting-as-a-host-address-book-provider.md)
  
## <a name="see-also"></a>Consulte también



[IABLogon : IUnknown](iablogoniunknown.md)

