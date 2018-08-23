---
title: Que actúa como un proveedor de libreta de direcciones externa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cafc6e3b6d863a7c2acec5811bf161ad0cd64458
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570033"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Que actúa como un proveedor de libreta de direcciones externa

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor externo es un proveedor de la libreta de direcciones que: 
  
- Asigna identificadores de plantilla para sus destinatarios.
    
- Admite el método [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) . 
    
- Proporciona el código para el mantenimiento de los destinatarios que existen en los contenedores de otros proveedores de libreta de direcciones conocidos como proveedores de host. Este código implica un objeto property, normalmente una **IMAPIProp** implementación de interfaz, que se ajusta un objeto property desde el proveedor de host. 
    
Actuar como un proveedor externo es una función opcional; No todos los proveedores deben admitir identificadores de plantilla y su código relacionado. Implementar un proveedor como un proveedor externo si desea mantener el control sobre los destinatarios que los proveedores de host crean con plantillas suministradas por el proveedor. 
  
El formato que usa el proveedor para sus identificadores de entrada también puede usarse para sus identificadores de plantilla. Identificadores de plantilla deben incluir registrado de su proveedor **MAPIUID** para habilitar MAPI enlazar correctamente los destinatarios a los proveedores de adecuados. 
  
MAPI llama a **IABLogon::OpenTemplateID** (método) su proveedor cuando un proveedor de host llama [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). El proveedor de host pasa el identificador de plantilla del destinatario en el parámetro _lpTemplateID_ en su llamada a **IMAPISupport::OpenTemplateID**. MAPI determina que el identificador de plantilla pertenece a su proveedor mediante la coincidencia de [MAPIUID](mapiuid.md) en el identificador de plantilla con el **MAPIUID** que su proveedor registrado en tiempo de inicio de sesión. MAPI, a continuación, reenvía la llamada del proveedor de host a su proveedor de a través del método **IABLogon::OpenTemplateID** . 
  
El proveedor de host también pasa un puntero a su implementación de objeto de la propiedad para el destinatario en el parámetro _lpMAPIPropData_ , un identificador de interfaz en el parámetro _lpInterface_ que corresponde al tipo de implementación de la interfaz que se pasan en _lpMAPIPropData_y un indicador opcional, FILL_ENTRY. Se espera que el proveedor para devolver en el parámetro _lppMAPIPropNew_ un puntero a una implementación de objeto de la propiedad del tipo especificado en _lpInterface_. El puntero devuelto puede ser al objeto ajustado (propiedad) implementada por el proveedor o para el objeto proporcionado por el proveedor de host en _lpMAPIPropData_. Su proveedor debe devolver un puntero de objeto de propiedad ajustado cuando:
  
- Tabla de presentación del destinatario contiene controles de cuadro de lista.
    
- La dirección de correo electrónico para el destinatario debe montarse desde los datos en varios controles de tabla para mostrar.
    
- Los problemas de proveedor Mostrar notificaciones de tabla.
    
El indicador FILL_ENTRY indica a su proveedor de que el proveedor de host requiere todas las propiedades del destinatario para actualizarse. Su proveedor es necesario para cumplir con esta solicitud.
  
Cuando un proveedor de host llama al método **OpenTemplateID** de su proveedor, es posible que su proveedor: 
  
- Actualizar periódicamente los datos para una entrada de copiado.
    
- Mantener una entrada copiada sincronizada con su original, por ejemplo, cuando se copia una entrada de la libreta de direcciones a la libreta de direcciones personales.
    
- Implementar la funcionalidad que no se pueden implementar por el proveedor de host, como rellenar dinámicamente lista cuadros en la tabla de detalles de la entrada copiada desde los datos en un servidor.
    
- Controlar la interacción entre las propiedades de una entrada copiada o ha creado una instancia de plantilla. Por ejemplo, los sistemas **PR_EMAIL_ADDRESS** de otras propiedades que se muestran en la tabla de detalles. 
    
Los dos primeros elementos son ejemplos de tareas que no requieren su proveedor suministrar un objeto property ajustado: una implementación de **IMAPIProp** que se basa en la implementación del proveedor de host. El proveedor simplemente puede actualizar las propiedades como devuelto y es necesario establecer el parámetro _lppMAPIPropNew_ para que apunte al puntero que se pasó por el proveedor de host en el parámetro _lpMAPIPropData_ . 
  
El segundo lugar dos tareas que requieren que el proveedor devuelva al proveedor de host un objeto de propiedad que se ajusta el objeto del proveedor de host con una funcionalidad adicional, como la capacidad para mostrar una hoja de propiedades para la entrada. Este objeto de la propiedad será una mensajería usuario o lista de distribución, según el tipo de objeto que se pasó por el proveedor de host en el parámetro _lpMAPIPropData_ e indicada por el identificador de interfaz en el parámetro _lpInterface_ . Si el parámetro _lpMAPIPropData_ señala a un usuario de mensajería, objeto ajustado (propiedad) de su proveedor debe ser una implementación de **IMailUser** . Si _lpMAPIPropData_ apunta a una lista de distribución, debe ser una implementación de **IDistList** . 
  
Objeto ajustado (propiedad) de su proveedor intercepta las llamadas al método **IMAPIProp** para llevar a cabo la manipulación de específicos del contexto del destinatario del proveedor de host, el objeto se ajuste. MAPI sólo tiene un requisito para objetos property ajustado: todas las llamadas a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) que solicita la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) se pasan al proveedor de host. Implementación de su proveedor puede usar el objeto table devuelto para interceptar las notificaciones de tabla para mostrar o para agregar su propio si es necesario. 
  
La siguiente lista incluye las tareas que normalmente se implementan en el objeto de propiedad ajustado implementado por proveedores externos:
  
- Preprocesamiento y procesamiento posterior de los valores de propiedad para el destinatario de host en [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Detalles de tratamiento de mostrar los controles de la tabla, como botones y cuadros de lista, en **IMAPIProp::OpenProperty**.
    
- Validar o manipular los valores de propiedad para el destinatario de host en [IMAPIProp::SetProps](imapiprop-setprops.md).
    
- Los sistemas de propiedades necesarias como **PR_EMAIL_ADDRESS** y comprobar que todas las propiedades necesarias se han establecido antes de guardar al destinatario de host en [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
### <a name="to-implement-iablogonopentemplateid"></a>Para implementar IABLogon::OpenTemplateID
  
1. Compruebe si el identificador de plantilla se pasa en con el parámetro _lpTemplateID_ es válido y se encuentra en un formato que el proveedor reconoce. Si no es así, se producirá un error y devolver MAPI_E_INVALID_ENTRYID. 
    
2. Crear un objeto del tipo indicado por el identificador de plantilla, un usuario de mensajería, una lista de distribución o un destinatario de uso único. 
    
3. Llame al método **IUnknown:: AddRef** en el objeto de propiedad del proveedor de host, que es el objeto al que señala el parámetro _lpMAPIPropData_ . 
    
4. Si el parámetro _ulTemplateFlags_ se establece en FILL_ENTRY: 
    
   1. Si el nuevo objeto es una lista de distribución o de usuario de mensajería:
      
      1. Recuperar todas las propiedades del nuevo objeto, posiblemente mediante una llamada a su método **IMAPIProp::GetProps** . 
          
      2. Llamar al método **IMAPIProp::SetProps** del proveedor de host para copiar todas las propiedades devueltas al objeto de la propiedad del proveedor de host. 
      
   2. Si el nuevo objeto es un destinatario de uso único, llamar al método **IMAPIProp::SetProps** del proveedor de host para establecer las propiedades siguientes: 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para el tipo de dirección controlado por el proveedor.
        
      - **Precio:\_identificador de plantilla** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) para el identificador de plantilla de los parámetros _lpTemplateID_ y _cbTemplateID_ . 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) a DT_MAILUSER o DT_DISTLIST, según corresponda.
    
5. Establecer el contenido del parámetro _lppMAPIPropNew_ para que apunte al nuevo objeto de su proveedor o el objeto de la propiedad pasado con el parámetro _lpMAPIPropData_ , dependiendo de si su proveedor determina que es necesario un objeto ajustado. 
    
6. Si se produce un error crítico, como un error de red o una condición de falta de memoria, devolver el valor de error apropiado. Este valor debe obtener propaga al cliente con la estructura [MAPIERROR](mapierror.md) apropiado, una tarea realizada por el proveedor de host. 
    

