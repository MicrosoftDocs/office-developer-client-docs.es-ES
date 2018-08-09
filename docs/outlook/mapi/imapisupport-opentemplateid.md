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
ms.openlocfilehash: f99843bcdf3689acad72145a33d6a9804175a413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817539"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**Hace referencia a**: Outlook 
  
Se abre una entrada del destinatario en un proveedor de libreta de direcciones externa.
  
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
  
> [entrada] El número de bytes en el identificador de plantilla que señala _lpTemplateID_. 
    
 _lpTemplateID_
  
> [entrada] Un puntero al identificador de plantilla **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) (propiedad) de la entrada del destinatario que se va a abrir.
    
 _ulTemplateFlags_
  
> [entrada] Una máscara de bits de indicadores que se utilizan para describir cómo abrir la entrada. Se puede establecer la marca siguiente:
    
FILL_ENTRY 
  
> Se creará una nueva entrada. Cuando el proveedor externo recibe la llamada de [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) posterior de MAPI, puede controlar cómo se creó la entrada mediante la modificación de las propiedades que señala el parámetro _lpMAPIPropData_ o devolviendo una interfaz específica implementación en _lppMAPIPropNew_ para controlar cómo se establecen las propiedades de la nueva entrada. 
    
 _lpMAPIPropData_
  
> [entrada] Un puntero a la implementación de la interfaz que el autor de la llamada se usa para tener acceso a la entrada. Ésta es la implementación que el proveedor externo puede ajustar con su propia implementación y devolver en el parámetro _lppMAPIPropNew_ . El parámetro _lpMAPIPropData_ debe apuntar a una implementación de la interfaz de lectura y escritura que se deriva de [IMAPIProp: IUnknown](imapipropiunknown.md) y es compatible con la interfaz que se solicita en el parámetro _lpInterface_ . 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la entrada. El parámetro _lppMAPIPropNew_ apunta a una interfaz del tipo especificado por _lpInterface_. Pasando NULL, devuelve la interfaz estándar para un usuario de mensajería, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> [out] Un puntero a la implementación de la interfaz que suministra el proveedor externo para obtener acceso a la entrada.
    
 _lpMAPIPropSibling_
  
> Reservado; debe ser NULL.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de enlace fue correcto.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El proveedor de libreta de direcciones externa no existe.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::OpenTemplateID** se implementa sólo para los objetos de compatibilidad con de proveedor de la libreta de direcciones. Se denomina **OpenTemplateID** sólo por los proveedores de la libreta de direcciones que pueden actuar como hosts para las entradas que pertenecen a otros proveedores de libreta de direcciones, también conocido como externos proveedores. Proveedores de host llame a **OpenTemplateID** para abrir una entrada externa, que se produce cuando se enlazan datos en el proveedor de host al código en el proveedor extranjero. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llamar a **OpenTemplateID** sólo si se admite el almacenamiento de entradas con identificadores de plantilla desde los proveedores de la libreta de direcciones externa. Este soporte coloca los requisitos adicionales en sus implementaciones de [IABContainer::CreateEntry](iabcontainer-createentry.md) y [IABLogon::OpenEntry](iablogon-openentry.md) . Para obtener más información, consulte las descripciones de estos métodos y [actúa como un proveedor de libreta de direcciones de Host](acting-as-a-host-address-book-provider.md).
  
Si la llamada **OpenTemplateID** devuelve como la interfaz enlazada la misma implementación de objeto de propiedad que pasa en, puede liberar la referencia al objeto (propiedad). Esto es debido a que el proveedor externo ha llamado al método del objeto **AddRef** para mantener su propia referencia. Si el proveedor externo no es necesario mantener una referencia al objeto de la propiedad, **OpenTemplateID** devolverá el objeto de propiedad independiente. 
  
Si se produce un error en **OpenTemplateID** con MAPI_E_UNKNOWN_ENTRYID, intente continuar por el tratamiento de la entrada como de solo lectura. 
  
## <a name="see-also"></a>Vea también



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propiedad canónica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

