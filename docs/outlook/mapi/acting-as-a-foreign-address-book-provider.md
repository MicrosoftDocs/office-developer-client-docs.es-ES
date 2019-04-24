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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331215"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Actuar como un proveedor de libreta de direcciones externo

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor externo es un proveedor de libreta de direcciones que: 
  
- Asigna identificadores de plantilla para sus destinatarios.
    
- Admite el método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) . 
    
- Proporciona código para mantener destinatarios que existen en los contenedores de otros proveedores de libretas de direcciones conocidos como proveedores de host. Este código implica un objeto Property, normalmente una implementación de interfaz **IMAPIProp** , que ajusta un objeto Property desde el proveedor de host. 
    
Actuar como proveedor externo es un rol opcional; no todos los proveedores necesitan admitir identificadores de plantilla y el código relacionado. Implemente el proveedor como proveedor externo si desea mantener el control sobre los destinatarios que los proveedores de hosts crean mediante plantillas proporcionadas por el proveedor. 
  
El formato que su proveedor usa para sus identificadores de entrada también puede usarse para sus identificadores de plantilla. Los identificadores de plantilla deben incluir la **MAPIUID** registrada del proveedor para permitir que MAPI enlace correctamente los destinatarios a los proveedores apropiados. 
  
MAPI llama al método **IABLogon:: OpenTemplateID** del proveedor cuando un proveedor de host llama a [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md). El proveedor de host pasa el identificador de la plantilla del destinatario en el parámetro _lpTemplateID_ en su llamada a **IMAPISupport:: OpenTemplateID**. MAPI determina que el identificador de plantilla pertenece al proveedor al hacer coincidir el [MAPIUID](mapiuid.md) del identificador de la plantilla con el **MAPIUID** que el proveedor registró en el momento de iniciar la sesión. MAPI, a continuación, reenvía la llamada del proveedor de host a su proveedor a través del método **IABLogon:: OpenTemplateID** . 
  
El proveedor de host también pasa un puntero a su implementación de objeto Property para el destinatario en el parámetro _lpMAPIPropData_ , un identificador de interfaz en el parámetro _lpInterface_ que corresponde al tipo de implementación de interfaz. se pasa en _lpMAPIPropData_y un indicador opcional, FILL_ENTRY. Se espera que el proveedor devuelva en el parámetro _lppMAPIPropNew_ un puntero a una implementación de objeto Property del tipo especificado en _lpInterface_. El puntero devuelto puede estar en el objeto de propiedad ajustado implementado por el proveedor o con el objeto proporcionado por el proveedor de host en _lpMAPIPropData_. El proveedor debe devolver un puntero de objeto de propiedad ajustada cuando:
  
- La tabla de presentación del destinatario contiene controles de cuadro de lista.
    
- La dirección de correo electrónico del destinatario debe ensamblarse a partir de los datos en varios controles de la tabla de visualización.
    
- Los problemas de su proveedor muestran las notificaciones de tabla.
    
La marca FILL_ENTRY indica al proveedor que el proveedor de host requiere que se actualicen todas las propiedades del destinatario. El proveedor es necesario para completar esta solicitud.
  
Cuando un proveedor de host llama al método **OpenTemplateID** de su proveedor, el proveedor puede: 
  
- Actualizar periódicamente los datos de una entrada copiada.
    
- Mantener una entrada copiada sincronizada con su original, por ejemplo, cuando se copia una entrada de la libreta de direcciones en la libreta personal de direcciones.
    
- Implementar funcionalidad que no puede ser implementada por el proveedor de host, como rellenar dinámicamente cuadros de lista en la tabla de detalles de la entrada que se ha copiado de los datos en un servidor.
    
- Controlar la interacción entre las propiedades de una entrada o una plantilla de instancia copiada. Por ejemplo, el cálculo de **PR_EMAIL_ADDRESS** de otras propiedades mostradas en la tabla de detalles. 
    
Los dos primeros elementos son ejemplos de tareas que no requieren que su proveedor suministre un objeto de propiedad ajustada: una implementación de **IMAPIProp** basada en la implementación del proveedor de host. El proveedor simplemente puede actualizar las propiedades según sea necesario y volver, estableciendo el parámetro _lppMAPIPropNew_ para que apunte al puntero pasado por el proveedor de host en el parámetro _lpMAPIPropData_ . 
  
Las dos tareas siguientes requieren que el proveedor vuelva al proveedor de host, un objeto Property que envuelve el objeto del proveedor de host con funcionalidad adicional, como la capacidad de mostrar una hoja de propiedades para la entrada. Este objeto Property será un usuario de mensajería o una lista de distribución, según el tipo de objeto pasado por el proveedor de host en el parámetro _lpMAPIPropData_ y indicado por el identificador de interfaz en el parámetro _lpInterface_ . Si el parámetro _lpMAPIPropData_ apunta a un usuario de mensajería, el objeto de propiedad ajustado del proveedor debe ser una implementación de **IMailUser** . Si _lpMAPIPropData_ apunta a una lista de distribución, debe ser una implementación de **IDistList** . 
  
El objeto de propiedad ajustado del proveedor intercepta las llamadas del método **IMAPIProp** para llevar a cabo la manipulación específica del contexto del destinatario del proveedor del host: el objeto que se va a ajustar. MAPI sólo tiene un requisito para los objetos de propiedad ajustada: todas las llamadas a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) que solicitan la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) deben pasarse al proveedor de host. La implementación de su proveedor puede usar la tabla devuelta para interceptar notificaciones de tabla de visualización o agregar sus propias notificaciones si es necesario. 
  
La siguiente lista incluye las tareas que se implementan normalmente en el objeto de propiedad ajustado implementado por proveedores externos:
  
- Valores de propiedad de preprocesamiento y postprocesamiento para el destinatario del host en [IMAPIProp:: GetProps](imapiprop-getprops.md).
    
- Al controlar los detalles, se muestran controles de tabla, como botones y cuadros de lista, en **IMAPIProp:: OpenProperty**.
    
- Validar o manipular valores de propiedad para el destinatario de host en [IMAPIProp:: SetProps](imapiprop-setprops.md).
    
- Calcule las propiedades requeridas como **PR_EMAIL_ADDRESS** y compruebe que se hayan establecido todas las propiedades necesarias antes de guardar el destinatario del host en [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
    
### <a name="to-implement-iablogonopentemplateid"></a>Para implementar IABLogon:: OpenTemplateID
  
1. Compruebe si el identificador de la plantilla que se ha pasado con el parámetro _lpTemplateID_ es válido y está en un formato reconocido por el proveedor. Si no es así, se produce un error y se devuelve MAPI_E_INVALID_ENTRYID. 
    
2. Cree un objeto del tipo indicado por el identificador de la plantilla, ya sea un usuario de mensajería, una lista de distribución o un destinatario de uso único. 
    
3. Llame al método **IUnknown:: AddRef** en el objeto Property del proveedor de host, que es el objeto al que apunta el parámetro _lpMAPIPropData_ . 
    
4. Si el parámetro _ulTemplateFlags_ está establecido en FILL_ENTRY: 
    
   1. Si el nuevo objeto es un usuario de mensajería o una lista de distribución:
      
      1. Recupere todas las propiedades del nuevo objeto, posiblemente llamando a su método **IMAPIProp:: GetProps** . 
          
      2. Llame al método **IMAPIProp:: SetProps** del proveedor de host para copiar todas las propiedades recuperadas en el objeto Property del proveedor de host. 
      
   2. Si el nuevo objeto es un destinatario de uso único, llame al método **IMAPIProp:: SetProps** del proveedor de host para establecer las siguientes propiedades: 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) al tipo de dirección administrado por el proveedor.
        
      - **PR\_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) al identificador de plantilla de los parámetros _lpTemplateID_ y _cbTemplateID_ . 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) a DT_MAILUSER o DT_DISTLIST, según corresponda.
    
5. Establezca el contenido del parámetro _lppMAPIPropNew_ para que apunte al nuevo objeto del proveedor o el objeto de la propiedad que se pasa con el parámetro _lpMAPIPropData_ , en función de si el proveedor determina que es necesario un objeto ajustado. 
    
6. Si se produce un error crítico, como un error de red o una condición de memoria insuficiente, devuelva el valor de error correspondiente. Este valor debe propagarse al cliente con la estructura [MAPIERROR](mapierror.md) adecuada, una tarea realizada por el proveedor de host. 
    

