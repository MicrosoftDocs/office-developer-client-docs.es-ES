---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334751"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una entrada de destinatario que tiene datos que residen en un proveedor de la libreta de direcciones de host.
  
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
  
> a El recuento de bytes en el identificador de plantilla al que apunta el parámetro _lpTemplateID_ . 
    
 _lpTemplateID_
  
> a Un puntero al identificador de la plantilla o a la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de la entrada del destinatario que se va a abrir.
    
 _ulTemplateFlags_
  
> a Máscara de la máscara usada para indicar cómo abrir la entrada representada por el identificador de la plantilla. Se puede establecer la siguiente marca:
    
FILL_ENTRY 
  
> El proveedor de host está creando una nueva entrada en su contenedor en función de la entrada representada por el identificador de la plantilla. El método **IABLogon:: OpenTemplateID** debe realizar la inicialización específica de la entrada del proveedor de host mediante la implementación de [IMAPIProp: IUnknown](imapipropiunknown.md) en el parámetro _lpMAPIPropData_ o devolver un **IMAPIProp personalizado **implementación de la interfaz en el parámetro _lppMAPIPropNew_ . 
    
 _lpMAPIPropData_
  
> a Un puntero al objeto Property del proveedor de host e implementación de una interfaz derivada de **IMAPIProp**.
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa el tipo de puntero de interfaz que se va a devolver en el parámetro _lppMAPIPropNew_ . Al pasar **null** , se devuelve la interfaz de usuario de mensajería estándar, [IMailUser: IMAPIProp](imailuserimapiprop.md).
    
 _lppMAPIPropNew_
  
> contempla Un puntero al objeto de propiedad enlazado y una implementación de una interfaz derivada de **IMAPIProp**.
    
 _lpMAPIPropSibling_
  
> contempla Reserve debe ser **null**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El código adecuado se ha enlazado correctamente a los datos relacionados en el proveedor de host.
    
MAPI_E_NO_SUPPORT 
  
> El objeto no admite identificadores de plantilla.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El proveedor de libreta de direcciones no reconoce el identificador de plantilla pasado en el parámetro _lpTemplateID_ . 
    
## <a name="remarks"></a>Comentarios

El método **IABLogon:: OpenTemplateID** solo se implementa por los proveedores de la libreta de direcciones que necesitan mantener el control sobre las copias de sus entradas que se encuentran en los contenedores de los proveedores de host. Los proveedores que implementan **OpenTemplateID** se conocen como proveedores de la libreta de direcciones externa. Los proveedores de host llaman a [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) para crear una entrada copiada o abrir la entrada copiada y MAPI pasa la llamada a **IABLogon:: OpenTemplateID**. **IABLogon:: OpenTemplateID** abre la entrada y enlaza el código que la controla a los datos en el proveedor de host. 
  
En lugar de usar un identificador de entrada, **IABLogon:: OpenTemplateID** usa otra propiedad, el identificador de plantilla de la entrada, **PR_TEMPLATEID**. Los identificadores de plantilla deben ser compatibles con las entradas cuyo código deba enlazarse a los datos de un proveedor de host.
  
Algunos ejemplos de Cuándo un proveedor de libreta de direcciones debe implementar **IABLogon:: OpenTemplateID** son los siguientes: 
  
- Para actualizar periódicamente los datos de una entrada copiada de modo que permanezca sincronizada con el original.
    
- Para implementar la funcionalidad que el proveedor de host no puede implementar, como llenar de forma dinámica una lista que aparece en la tabla de detalles de la entrada a partir de los datos de un servidor.
    
- Para controlar la interacción entre las propiedades de la entrada del proveedor de host y la entrada original, como calcular el **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) a partir de los valores de los controles de edición en la visualización de detalles que contienen diferentes componentes de la dirección.
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando un proveedor de host copia o crea una entrada de su proveedor y proporciona una implementación de objeto Property a través de **IABLogon:: OpenTemplateID**, controla la mayoría de las llamadas para mantener la entrada. Sin embargo, dado que es el proveedor de host el que puede reenviar las llamadas a usted, el proveedor de hosts puede interceptar cualquier llamada y realizar un procesamiento personalizado antes de reenviar la llamada.
  
Debe usar las siguientes instrucciones en las implementaciones de objetos de propiedad:
  
- Cuando se llama a [IMAPIProp:: GetProps](imapiprop-getprops.md) , determine si la solicitud es para una propiedad calculada y, si es así, controle. Transfiera todas las solicitudes de propiedades no calculadas al proveedor de host. 
    
- Cuando se llama a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir cualquier tabla excepto la tabla de visualización de detalles, administre la solicitud. La mayoría de las tablas no se pueden copiar con precisión en el proveedor de host. Debe generar la implementación de **IMAPITable** para estas tablas solicitadas. La tabla de detalles **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) propiedad debe copiarse en el proveedor de host. Esto permite a este proveedor generar la tabla de forma local. Es posible que desee incluir la implementación de la tabla de visualización para generar notificaciones de tabla de visualización. 
    
- Cuando se llama a [IMAPIProp:: SetProps](imapiprop-setprops.md) , el proveedor de host puede validar los datos antes de permitir que establezca las propiedades. Puede comprobar que se han establecido o calculado todas las propiedades necesarias. Si se detecta un error, devuelva el valor de error adecuado y, si es posible, una explicación adicional a [IMAPIProp:: GetLastError](imapiprop-getlasterror.md).
    
- Cuando se llama a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , es posible que el proveedor de host desee realizar el procesamiento antes de guardar la entrada. Debe guardar todos los datos que se vean afectados por las propiedades modificadas, como una nueva dirección, en la entrada del proveedor de host. 
    
En general, haga que la implementación de la entrada que pasa al proveedor de host intercepte todos los métodos para realizar una manipulación específica del contexto de las propiedades relevantes. Si la marca FILL_ENTRY se pasa en el parámetro _ulTemplateFlags_ , establezca todas las propiedades de la entrada. 
  
Si devuelve un nuevo objeto Property en el parámetro _lppMAPIPropNew_ , llame al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del objeto Property del proveedor de host para mantener una referencia. Todas las llamadas a través del objeto enlazado que la implementación de **IMAPIProp** devueltos en _lppMAPIPropNew_ deben enrutarse a su método correspondiente en el objeto de la propiedad host después de que se trate con el objeto enlazado. 
  
Los identificadores de propiedad de las propiedades con nombre que se pasan a través del objeto de propiedad enlazado están en el espacio de nombres del identificador del proveedor. La implementación del método [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) debe determinar los nombres de las propiedades para que pueda realizar cualquier tarea específica de la plantilla. De forma similar, las propiedades que el proveedor pasa al proveedor de host también deben estar en el espacio de nombres. Por ejemplo, si establece una propiedad con nombre en **OpenTemplateID**, debe usar uno de sus identificadores para el nombre, creando si es necesario, llamando al método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
Si no reconoce el identificador de entrada que se ha pasado en _lpTemplateID_, devuelva MAPI_E_UNKNOWN_ENTRYID.
  
Para obtener más información acerca de cómo trabajar con identificadores de plantillas de la libreta de direcciones, consulte [actuar como un proveedor de libreta de direcciones externa](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Vea también



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propiedad canónica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

