---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418508"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una entrada de destinatario en un proveedor de libreta de direcciones externo.
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Parámetros

 _cbTemplateID_
  
> [entrada] El recuento de bytes en el identificador de plantilla al que apunta  _lpTemplateID_. 
    
 _lpTemplateID_
  
> [entrada] Puntero al identificador de plantilla **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de la entrada de destinatario que se va a abrir.
    
 _ulTemplateFlags_
  
> [entrada] Máscara de bits de marcas que se usa para describir cómo abrir la entrada. Se puede establecer la siguiente marca:
    
FILL_ENTRY 
  
> Se está creando una nueva entrada. Cuando el proveedor externo recibe la llamada [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) posterior de MAPI, puede controlar cómo se crea la entrada modificando las propiedades a las que apunta el parámetro  _lpMAPIPropData_ o devolviendo una implementación de interfaz específica en  _lppMAPIPropNew_ para controlar cómo se establecen las propiedades de la nueva entrada. 
    
 _lpMAPIPropData_
  
> [entrada] Puntero a la implementación de la interfaz que el autor de la llamada usa para obtener acceso a la entrada. Esta es la implementación que el proveedor externo puede encapsular con su propia implementación y devolver en el parámetro _lppMAPIPropNew._ El _parámetro lpMAPIPropData_ debe apuntar a una implementación de interfaz de lectura y escritura que deriva de [IMAPIProp : IUnknown](imapipropiunknown.md) y admite la interfaz que se solicita en el parámetro _lpInterface._ 
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la entrada. El  _parámetro lppMAPIPropNew_ apunta a una interfaz del tipo especificado por  _lpInterface_. Pasar NULL devuelve la interfaz estándar para un usuario de mensajería, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> [salida] Puntero a la implementación de la interfaz que proporciona el proveedor externo para obtener acceso a la entrada.
    
 _lpMAPIPropSibling_
  
> Reservado; debe ser NULL.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de enlace se ha realizado correctamente.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El proveedor de libreta de direcciones externo no existe.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::OpenTemplateID** solo se implementa para objetos de compatibilidad del proveedor de libreta de direcciones. **OpenTemplateID** solo lo llaman los proveedores de libretas de direcciones que pueden actuar como hosts para las entradas que pertenecen a otros proveedores de libretas de direcciones, también conocidos como proveedores externos. Los proveedores de host llaman a **OpenTemplateID** para abrir una entrada externa, que se produce cuando los datos del proveedor de host están enlazados al código del proveedor externo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame **a OpenTemplateID** solo si admite el almacenamiento de entradas con identificadores de plantilla de proveedores de libretas de direcciones externos. Esta compatibilidad coloca requisitos adicionales en las implementaciones [IABContainer::CreateEntry](iabcontainer-createentry.md) e [IABLogon::OpenEntry.](iablogon-openentry.md) Para obtener más información, vea las descripciones de estos métodos y [actuar como proveedor de libretas de direcciones de host.](acting-as-a-host-address-book-provider.md)
  
Si la **llamada a OpenTemplateID** devuelve como interfaz enlazada la misma implementación de objeto de propiedad que pasó, puede liberar la referencia al objeto de propiedad. Esto se debe a que el proveedor externo ha llamado al método **AddRef** del objeto para mantener su propia referencia. Si el proveedor externo no necesita mantener una referencia al objeto de propiedad, **OpenTemplateID** devolverá el objeto de propiedad independiente. 
  
Si Se produce un error en **OpenTemplateID** MAPI_E_UNKNOWN_ENTRYID, intente continuar tratando la entrada como de solo lectura. 
  
## <a name="see-also"></a>Consulte también



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propiedad canónica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

