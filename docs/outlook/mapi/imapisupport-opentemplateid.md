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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326365"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una entrada de destinatario en un proveedor de libreta de direcciones externa.
  
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

## <a name="parameters"></a>Parameters

 _cbTemplateID_
  
> a El recuento de bytes en el identificador de la plantilla apuntado por _lpTemplateID_. 
    
 _lpTemplateID_
  
> a Un puntero a la propiedad de **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) del identificador de plantilla de la entrada del destinatario que se va a abrir.
    
 _ulTemplateFlags_
  
> a Una máscara de máscara de marcas usada para describir cómo abrir la entrada. Se puede establecer la siguiente marca:
    
FILL_ENTRY 
  
> Se está creando una nueva entrada. Cuando el proveedor externo recibe la llamada subsiguiente a [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) de MAPI, puede controlar cómo se crea la entrada modificando las propiedades a las que apunta el parámetro _lpMAPIPropData_ o devolviendo una interfaz específica implementación de _lppMAPIPropNew_ para controlar cómo se establecen las propiedades de la nueva entrada. 
    
 _lpMAPIPropData_
  
> a Un puntero a la implementación de interfaz que el autor de la llamada usa para obtener acceso a la entrada. Esta es la implementación que el proveedor externo puede ajustar con su propia implementación y volver al parámetro _lppMAPIPropNew_ . El parámetro _lpMAPIPropData_ debe apuntar a una implementación de interfaz de lectura y escritura que derive de [IMAPIProp: IUnknown](imapipropiunknown.md) y admita la interfaz que se solicita en el parámetro _lpInterface_ . 
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la entrada. El parámetro _lppMAPIPropNew_ apunta a una interfaz del tipo especificado por _lpInterface_. Al pasar NULL, se devuelve la interfaz estándar de un usuario de mensajería, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> contempla Un puntero a la implementación de interfaz que el proveedor externo proporciona para obtener acceso a la entrada.
    
 _lpMAPIPropSibling_
  
> Reserve debe ser NULL.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de enlace se realizó correctamente.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El proveedor de la libreta de direcciones externa no existe.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: OpenTemplateID** solo se implementa para los objetos de compatibilidad del proveedor de la libreta de direcciones. Solo los proveedores de libreta de direcciones que pueden actuar como hosts de las entradas que pertenecen a otros proveedores de libretas de direcciones, también conocidos como proveedores externos, llaman a **OpenTemplateID** . Los proveedores de host llaman a **OpenTemplateID** para abrir una entrada externa, que se produce cuando los datos del proveedor de host están enlazados al código en el proveedor externo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame a **OpenTemplateID** solo si admite el almacenamiento de entradas con identificadores de plantilla de proveedores de la libreta de direcciones externa. Dicha compatibilidad incluye requisitos adicionales en las implementaciones de [IABContainer:: CreateEntry](iabcontainer-createentry.md) y [IABLogon:: OpenEntry](iablogon-openentry.md) . Para obtener más información, vea las descripciones de estos métodos y [actuar como un proveedor de la libreta de direcciones de host](acting-as-a-host-address-book-provider.md).
  
Si la llamada **OpenTemplateID** devuelve como interfaz enlazada la misma implementación de objeto Property que ha pasado, puede liberar la referencia al objeto Property. Esto se debe a que el proveedor externo ha llamado al método **AddRef** del objeto para mantener su propia referencia. Si el proveedor externo no necesita mantener una referencia al objeto Property, **OpenTemplateID** devolverá el objeto de propiedad independiente. 
  
Si **OpenTemplateID** produce un error con MAPI_E_UNKNOWN_ENTRYID, intente continuar tratando la entrada como de solo lectura. 
  
## <a name="see-also"></a>Vea también



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propiedad canónica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

