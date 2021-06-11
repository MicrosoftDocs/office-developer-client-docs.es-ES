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
  
Abre una entrada de destinatario que tiene datos que residen en un proveedor de libreta de direcciones host.
  
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
  
> [in] Recuento de bytes en el identificador de plantilla al que apunta el _parámetro lpTemplateID._ 
    
 _lpTemplateID_
  
> [in] Puntero al identificador de plantilla o **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de la entrada de destinatario que se va a abrir.
    
 _ulTemplateFlags_
  
> [in] Máscara de bits de marcas usadas para indicar cómo abrir la entrada representada por el identificador de plantilla. Se puede establecer la siguiente marca:
    
FILL_ENTRY 
  
> El proveedor de host está creando una nueva entrada en su contenedor en función de la entrada representada por el identificador de plantilla. El método **IABLogon::OpenTemplateID** debe realizar una inicialización específica de la entrada del proveedor de host mediante la implementación [IMAPIProp : IUnknown](imapipropiunknown.md) en el parámetro _lpMAPIPropData_ o devolver una implementación de interfaz **IMAPIProp** personalizada en el parámetro _lppMAPIPropNew._ 
    
 _lpMAPIPropData_
  
> [in] Puntero al objeto de propiedad del proveedor de host e implementación de una interfaz derivada de **IMAPIProp**.
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa el tipo de puntero de interfaz que se devolverá en el parámetro _lppMAPIPropNew._ Si **se pasa null,** se devuelve la interfaz de usuario de mensajería estándar, [IMailUser : IMAPIProp](imailuserimapiprop.md).
    
 _lppMAPIPropNew_
  
> [salida] Puntero al objeto de propiedad enlazado y una implementación de una interfaz derivada de **IMAPIProp**.
    
 _lpMAPIPropSibling_
  
> [salida] Reservado; debe ser **null**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El código adecuado se enlaza correctamente a datos relacionados en el proveedor de host.
    
MAPI_E_NO_SUPPORT 
  
> El objeto no admite los IDs de plantilla.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> El proveedor de libreta de direcciones no reconoce el identificador de plantilla pasado en el parámetro _lpTemplateID._ 
    
## <a name="remarks"></a>Comentarios

El **método IABLogon::OpenTemplateID** solo lo implementan los proveedores de libreta de direcciones que necesitan mantener el control sobre las copias de sus entradas que se encuentran en los contenedores de los proveedores de host. Los proveedores que implementan **OpenTemplateID** se conocen como proveedores de libretas de direcciones externos. Los proveedores de host llaman a [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para crear una entrada copiada o abrir la entrada copiada, y MAPI pasa la llamada a **IABLogon::OpenTemplateID**. **IABLogon::OpenTemplateID** abre la entrada y enlaza el código que la controla a los datos del proveedor de host. 
  
En lugar de usar un identificador de entrada, **IABLogon::OpenTemplateID** usa otra propiedad, el identificador de plantilla de la **entrada, PR_TEMPLATEID**. Los identificadores de plantilla deben ser compatibles con entradas cuyo código debe enlazarse a datos en un proveedor de host.
  
Algunos ejemplos de cuándo un proveedor de libreta de direcciones debe implementar **IABLogon::OpenTemplateID** son los siguientes: 
  
- Para actualizar periódicamente los datos de una entrada copiada de modo que se mantenga sincronizado con el original.
    
- Para implementar funciones que el proveedor de host no puede implementar, como rellenar dinámicamente una lista que aparece en la tabla de detalles de la entrada a partir de datos de un servidor.
    
- Para controlar la interacción entre las propiedades de la entrada del proveedor de host y la entrada original, como calcular **el PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) a partir de los valores de los controles de edición en la presentación de detalles que contienen diferentes componentes de la dirección.
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando un proveedor de host copia o crea una entrada del proveedor y proporciona una implementación de objeto de propiedad a través de **IABLogon::OpenTemplateID,** controla la mayoría de las llamadas para mantener la entrada. Sin embargo, dado que es el proveedor de host el que le reenvía estas llamadas, el proveedor de host puede interceptar cualquier llamada y realizar un procesamiento personalizado antes de reenviar la llamada.
  
Debe usar las siguientes directrices en las implementaciones de objetos de propiedad:
  
- Cuando se llama a [IMAPIProp::GetProps,](imapiprop-getprops.md) determine si la solicitud es para una propiedad calculada y, si es así, controlarla. Transferir todas las solicitudes de propiedades no comedida al proveedor de host. 
    
- Cuando [se llama a IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir cualquier tabla excepto la tabla para mostrar detalles, controla la solicitud. La mayoría de las tablas no se pueden copiar con precisión en el proveedor de host. Debe generar la implementación **de IMAPITable** para estas tablas solicitadas. La tabla de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) debe copiarse en el proveedor de host. Esto permite a este proveedor generar la tabla localmente. Es posible que desee ajustar la implementación de la tabla para mostrar para generar notificaciones de tabla para mostrar. 
    
- Cuando [se llama a IMAPIProp::SetProps,](imapiprop-setprops.md) el proveedor de host puede validar los datos antes de permitirle establecer las propiedades. Puede comprobar que todas las propiedades necesarias se han establecido o calculado. Si se detecta un error, devuelva el valor de error adecuado y, si puede, cualquier explicación adicional a través de [IMAPIProp::GetLastError](imapiprop-getlasterror.md).
    
- Cuando [se llama a IMAPIProp::SaveChanges,](imapiprop-savechanges.md) es posible que el proveedor de host desee realizar el procesamiento antes de guardar la entrada. Debe guardar los datos que se ven afectados por las propiedades modificadas, como una nueva dirección, en la entrada del proveedor de host. 
    
En general, realice la implementación de la entrada que pase de nuevo al proveedor de host interceptar todos los métodos para realizar una manipulación específica del contexto de las propiedades relevantes. Si la FILL_ENTRY se pasa en el  _parámetro ulTemplateFlags,_ establezca todas las propiedades de la entrada. 
  
Si devuelve un nuevo objeto de propiedad en el parámetro  _lppMAPIPropNew,_ llame al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del objeto de propiedad del proveedor de host para mantener una referencia. Todas las llamadas a través del objeto enlazado que la implementación **IMAPIProp** devuelta en  _lppMAPIPropNew_ se deben enrutar a su método correspondiente en el objeto de propiedad host después de que el objeto enlazado las ocupe. 
  
Los identificadores de propiedad de las propiedades con nombre que se pasan a través del objeto de propiedad enlazada se encuentran en el espacio de nombres de identificador del proveedor. La implementación del método [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) debe determinar los nombres de las propiedades para que pueda realizar tareas específicas de plantilla. Del mismo modo, las propiedades que el proveedor pasa al proveedor de host también deben estar en el espacio de nombres. Por ejemplo, si establece una propiedad con nombre en **OpenTemplateID,** debe usar uno de los identificadores para el nombre, para crearla, si es necesario, llamando al método [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) 
  
Si no reconoce el identificador de entrada pasado en  _lpTemplateID,_ devuelva MAPI_E_UNKNOWN_ENTRYID.
  
Para obtener más información acerca de cómo trabajar con identificadores de plantilla de libreta de direcciones, vea [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Vea también



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propiedad canónica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

