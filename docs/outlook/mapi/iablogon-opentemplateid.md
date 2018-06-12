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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: f2fedd98fe84d7359aebaca8d03a20f392dae2b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817111"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**Se aplica a**: Outlook 
  
Se abre una entrada del destinatario que tiene datos que residen en un proveedor de libreta de direcciones de host.
  
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

## <a name="parameters"></a>Sintaxis

 _cbTemplateID_
  
> [entrada] El número de bytes en el identificador de plantilla indicado por el parámetro _lpTemplateID_ . 
    
 _lpTemplateID_
  
> [entrada] Un puntero al identificador de plantilla, o la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), de la entrada del destinatario que se va a abrir.
    
 _ulTemplateFlags_
  
> [entrada] Una máscara de bits de indicadores que se utilizan para indicar cómo abrir la entrada representada por el identificador de plantilla. Se puede establecer la marca siguiente:
    
FILL_ENTRY 
  
> El proveedor de host está creando una nueva entrada en su contenedor en función de la entrada representada por el identificador de plantilla. El método **IABLogon::OpenTemplateID** ya sea debe realizar la inicialización específica de entrada del proveedor de host mediante el uso de la [IMAPIProp: IUnknown](imapipropiunknown.md) implementación en el parámetro _lpMAPIPropData_ o retorno personalizado **IMAPIProp **implementación en el parámetro _lppMAPIPropNew_ de la interfaz. 
    
 _lpMAPIPropData_
  
> [entrada] Un puntero al objeto de la propiedad del proveedor de host y la implementación de una interfaz deriva de **IMAPIProp**.
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa el tipo de puntero de interfaz que se devuelve en el parámetro _lppMAPIPropNew_ . Si se pasa **null** devuelve el estándar de mensajería de la interfaz de usuario, [IMailUser: IMAPIProp](imailuserimapiprop.md).
    
 _lppMAPIPropNew_
  
> [out] Un puntero al objeto de la propiedad enlazada y una implementación de una interfaz que se deriva de **IMAPIProp**.
    
 _lpMAPIPropSibling_
  
> [out] Reservado; debe ser **null**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El código correspondiente se enlazó correctamente a los datos relacionados en el proveedor de host.
    
MAPI_E_NO_SUPPORT 
  
> El objeto no es compatible con los identificadores de plantilla.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> No se reconoce el identificador de plantilla que se pasa en el parámetro _lpTemplateID_ por el proveedor de la libreta de direcciones. 
    
## <a name="remarks"></a>Notas

El método **IABLogon::OpenTemplateID** se implementa sólo por los proveedores de la libreta de direcciones que necesitan para mantener el control sobre las copias de sus entradas que se encuentran en los contenedores de los proveedores de host. Proveedores que implementan **OpenTemplateID** se conocen como los proveedores de la libreta de direcciones externa. Proveedores de host llame a [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para crear una entrada copiada o abrir la entrada copiada y MAPI se pasa en la llamada a **IABLogon::OpenTemplateID**. **IABLogon::OpenTemplateID** abre la entrada y enlaza el código que controla a los datos en el proveedor de host. 
  
En lugar de usar un identificador de entrada, **IABLogon::OpenTemplateID** usa otra propiedad, identificador de la plantilla de la entrada, **PR_TEMPLATEID**. Identificadores de plantilla deben admitirse en entradas cuyo código debe estar enlazado a datos en un proveedor de host.
  
Algunos ejemplos de cuándo un proveedor de la libreta de direcciones debe implementar **IABLogon::OpenTemplateID** son los siguientes: 
  
- Para actualizar los datos para una entrada de copiado periódicamente para que se mantenga sincronizada con el original.
    
- Para implementar la funcionalidad que no se puede implementar el proveedor de host, como rellenar dinámicamente una lista que aparece en la tabla de detalles de la entrada de datos en un servidor.
    
- Para controlar la interacción entre las propiedades de entrada del proveedor de host y la entrada original, como los sistemas de la **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) de los valores de los controles de edición en la pantalla de detalles que contienen diferentes componentes de la dirección.
    
## <a name="notes-to-implementers"></a>Notas para los implementadores

Cuando un proveedor de host copia o crea una entrada de su proveedor y proporcionar una implementación de objeto de la propiedad a través de **IABLogon::OpenTemplateID**, controlar la mayoría de las llamadas para mantener la entrada. Sin embargo, porque es el proveedor de host para reenviar estas llamadas a usted, el proveedor de host puede interceptar cualquier llamada y realizar un procesamiento personalizado antes de reenviar la llamada.
  
Debe usar las siguientes instrucciones en las implementaciones de objeto de la propiedad:
  
- Cuando se llama a [IMAPIProp::GetProps](imapiprop-getprops.md) , determine si la solicitud es para una propiedad calculada y, si es así, controlarla. Transferir todas las solicitudes de propiedades no calculadas para el proveedor de host. 
    
- Cuando se llama a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir cualquier tabla excepto los detalles de mostrar tabla, controlar la solicitud. La mayoría de las tablas no se puede copiar con exactitud para el proveedor de host. Debe generar la implementación de **IMAPITable** para estas tablas solicitadas. La propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de tabla de detalles debe copiarse en el proveedor de host. Esto permite que este proveedor generar la tabla localmente. Es posible que desee ajustar la implementación de la tabla para mostrar para generar notificaciones de tabla para mostrar. 
    
- Cuando se llama a [IMAPIProp::SetProps](imapiprop-setprops.md) , el proveedor de host puede validar los datos antes de lo que le permite establecer las propiedades. Puede comprobar que todas las propiedades necesarias se han establecido o calculado. Si se detecta un error, devuelva el valor de error apropiado y, si es posible, cualquier explicación adicional a través de [IMAPIProp::GetLastError](imapiprop-getlasterror.md).
    
- Cuando se llama a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , el proveedor de host es posible que desee realizar un procesamiento antes de guardar la entrada. Debe guardar todos los datos que se ve afectados por las propiedades modificadas, como una dirección nueva, en la entrada del proveedor de host. 
    
En general, hacer que la implementación de la entrada que se pasa al proveedor de host todos los métodos para manipular los específicos del contexto de las propiedades relevantes intercept. Si la marca FILL_ENTRY se pasa en el parámetro _ulTemplateFlags_ , establezca todas las propiedades de la entrada. 
  
Si se devuelve un nuevo objeto property en el parámetro _lppMAPIPropNew_ , llame al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) del objeto de propiedad del proveedor de host para mantener una referencia. Todas las llamadas a través del objeto dependiente que devuelve la implementación de **IMAPIProp** en _lppMAPIPropNew_ deben enrutarse a su método correspondiente en el objeto de la propiedad host después de que se tratarán por el objeto dependiente. 
  
Los identificadores de propiedad de las propiedades con nombre que se pasan a través de su objeto dependiente (propiedad) se encuentran en el espacio de nombres de identificador del proveedor. La implementación del método [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) debe determinar los nombres de las propiedades de modo que pueda realizar las tareas específicas de las plantillas. De forma similar, también deben ser propiedades que pasa el proveedor el proveedor de host en el espacio de nombres. Por ejemplo, si establece una propiedad con nombre en **OpenTemplateID**, se debe utilizar uno de los identificadores para el nombre, crear, si es necesario, llamando al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
Si no reconoce el identificador de entrada que se pasan en _lpTemplateID_, devolver MAPI_E_UNKNOWN_ENTRYID.
  
Para obtener más información acerca de cómo trabajar con identificadores de plantilla de la libreta de direcciones, vea [actuar como un proveedor de libreta de direcciones externa](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Ver también



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propiedad canónico PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IABLogon: IUnknown](iablogoniunknown.md)

