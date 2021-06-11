---
title: Actuar como un proveedor de libreta de direcciones externo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 300681bd585e9d534113404a82f43565f4e79bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435743"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Actuar como un proveedor de libreta de direcciones externo

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor externo es un proveedor de libreta de direcciones que: 
  
- Asigna identificadores de plantilla para sus destinatarios.
    
- Admite el [método IABLogon::OpenTemplateID.](iablogon-opentemplateid.md) 
    
- Proporciona código para mantener los destinatarios que existen en los contenedores de otros proveedores de libretas de direcciones conocidos como proveedores de host. Este código implica un objeto de propiedad, normalmente una implementación de interfaz **IMAPIProp,** que encapsula un objeto de propiedad del proveedor de host. 
    
Actuar como proveedor externo es un rol opcional; no todos los proveedores necesitan admitir identificadores de plantilla y su código relacionado. Implemente su proveedor como proveedor externo si desea mantener el control sobre los destinatarios que los proveedores de host crean mediante plantillas proporcionadas por el proveedor. 
  
El formato que el proveedor usa para sus identificadores de entrada también se puede usar para sus identificadores de plantilla. Los identificadores de plantilla deben incluir **MAPIUID** registrado del proveedor para permitir que MAPI enlace correctamente a los destinatarios a los proveedores adecuados. 
  
MAPI llama al método **IABLogon::OpenTemplateID** del proveedor cuando un proveedor de host llama a [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). El proveedor de host pasa el identificador de plantilla del destinatario en el parámetro  _lpTemplateID_ en su llamada a **IMAPISupport::OpenTemplateID**. MAPI determina que el identificador de plantilla pertenece al proveedor al coincidir el [MAPIUID](mapiuid.md) en el identificador de plantilla con el **MAPIUID** que el proveedor registró en el momento del inicio de sesión. A continuación, MAPI reenvía la llamada del proveedor de host al proveedor mediante el **método IABLogon::OpenTemplateID.** 
  
El proveedor de host también pasa un puntero a su implementación de objeto de propiedad para el destinatario en el parámetro  _lpMAPIPropData,_ un identificador de interfaz en el parámetro  _lpInterface_ que corresponde al tipo de implementación de interfaz pasada en  _lpMAPIPropData_ y una marca opcional, FILL_ENTRY. Se espera que el proveedor devuelva en el parámetro  _lppMAPIPropNew_ un puntero a una implementación de objeto de propiedad del tipo especificado en  _lpInterface_. El puntero devuelto puede ser al objeto de propiedad ajustado implementado por el proveedor o al objeto proporcionado por el proveedor host en  _lpMAPIPropData_. El proveedor debe devolver un puntero de objeto de propiedad ajustada cuando:
  
- La tabla para mostrar del destinatario contiene controles de cuadro de lista.
    
- La dirección de correo electrónico del destinatario debe ensamblarse a partir de datos en varios controles de tabla para mostrar.
    
- El proveedor emite notificaciones de tabla para mostrar.
    
La FILL_ENTRY indica al proveedor que el proveedor de host requiere que se actualicen todas las propiedades del destinatario. Es necesario que el proveedor cumpla esta solicitud.
  
Cuando un proveedor de host llama al método **OpenTemplateID** del proveedor, el proveedor puede: 
  
- Actualice periódicamente los datos de una entrada copiada.
    
- Mantenga una entrada copiada sincronizada con su original, como cuando se copia una entrada de libreta de direcciones en la libreta de direcciones personal.
    
- Implemente funciones que el proveedor de host no puede implementar, como rellenar de forma dinámica cuadros de lista en la tabla de detalles de la entrada copiada a partir de datos de un servidor.
    
- Controlar la interacción entre las propiedades de una entrada copiada o una plantilla de creación de instancias. Por ejemplo, la informática **PR_EMAIL_ADDRESS** de otras propiedades que se muestran en la tabla de detalles. 
    
Los dos primeros elementos son ejemplos de tareas que no requieren que el proveedor proporcione un objeto de propiedad ajustado, una implementación de **IMAPIProp** basada en la implementación del proveedor de host. El proveedor simplemente puede actualizar las propiedades según sea necesario y devolver, estableciendo el parámetro _lppMAPIPropNew_ para que apunte al puntero pasado por el proveedor de host en el parámetro _lpMAPIPropData._ 
  
Las dos segundas tareas requieren que el proveedor devuelva al proveedor de host un objeto de propiedad que ajuste el objeto del proveedor de host con funciones adicionales, como la capacidad de mostrar una hoja de propiedades para la entrada. Este objeto de propiedad será un usuario de mensajería o una lista de distribución, según el tipo de objeto pasado por el proveedor de host en el parámetro _lpMAPIPropData_ e indicado por el identificador de interfaz en el parámetro _lpInterface._ Si el _parámetro lpMAPIPropData_ apunta a un usuario de mensajería, el objeto de propiedad ajustado del proveedor debe ser una **implementación de IMailUser.** Si _lpMAPIPropData_ apunta a una lista de distribución, debe ser una **implementación de IDistList.** 
  
El objeto de propiedad ajustado del proveedor intercepta llamadas al método **IMAPIProp** para realizar una manipulación específica del contexto del destinatario del proveedor de host, el objeto que está ajustando. MAPI solo tiene un requisito para objetos de propiedad ajustados: todas las llamadas a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) que solicitan la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) deben pasarse al proveedor de host. La implementación del proveedor puede usar la tabla devuelta para interceptar notificaciones de tabla para mostrar o para agregar las suyas propias si es necesario. 
  
La siguiente lista incluye tareas que normalmente se implementan en el objeto de propiedad ajustado implementado por proveedores externos:
  
- Valores de propiedades de preprocesamiento y postprocesamiento para el destinatario del host [en IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Los detalles de control muestran controles de tabla, como botones y cuadros de lista, **en IMAPIProp::OpenProperty**.
    
- Validar o manipular valores de propiedad para el destinatario del host [en IMAPIProp::SetProps](imapiprop-setprops.md).
    
- Calcular las propiedades **necesarias, como PR_EMAIL_ADDRESS** y comprobar que todas las propiedades necesarias se han establecido antes de guardar el destinatario del host en [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
### <a name="to-implement-iablogonopentemplateid"></a>Para implementar IABLogon::OpenTemplateID
  
1. Compruebe si el identificador de plantilla pasado con el parámetro  _lpTemplateID_ es válido y tiene un formato que el proveedor reconoce. Si no es así, falle y devuelva MAPI_E_INVALID_ENTRYID. 
    
2. Cree un objeto del tipo indicado por el identificador de plantilla, ya sea un usuario de mensajería, una lista de distribución o un destinatario único. 
    
3. Llame al **método IUnknown::AddRef** en el objeto de propiedad del proveedor de host, que es el objeto al que apunta el parámetro _lpMAPIPropData._ 
    
4. Si el  _parámetro ulTemplateFlags_ está establecido en FILL_ENTRY: 
    
   1. Si el nuevo objeto es un usuario de mensajería o una lista de distribución:
      
      1. Recupere todas las propiedades del nuevo objeto, posiblemente llamando a su **método IMAPIProp::GetProps.** 
          
      2. Llame al método **IMAPIProp::SetProps** del proveedor de host para copiar todas las propiedades recuperadas en el objeto de propiedad del proveedor de host. 
      
   2. Si el nuevo objeto es un destinatario único, llame al método **IMAPIProp::SetProps** del proveedor de host para establecer las siguientes propiedades: 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) al tipo de dirección que controla el proveedor.
        
      - **PR \_ TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) al identificador de plantilla de los parámetros _lpTemplateID_ y _cbTemplateID._ 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para DT_MAILUSER o DT_DISTLIST, según corresponda.
    
5. Establezca el contenido del parámetro  _lppMAPIPropNew_ para que apunte al nuevo objeto del proveedor o al objeto de propiedad pasado con el parámetro  _lpMAPIPropData,_ en función de si el proveedor determina que es necesario un objeto ajustado. 
    
6. Si se produce un error crítico, como un error de red o una condición de falta de memoria, devuelve el valor de error adecuado. Este valor debe propagarse al cliente con la estructura [MAPIERROR](mapierror.md) adecuada, una tarea realizada por el proveedor de host. 
    

