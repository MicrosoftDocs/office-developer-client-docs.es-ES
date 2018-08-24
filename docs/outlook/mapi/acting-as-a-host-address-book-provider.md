---
title: Actuar como un proveedor de libreta de direcciones host
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: de0acb88eee6addc0347f5281e5fbe5070bad0a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595414"
---
# <a name="acting-as-a-host-address-book-provider"></a>Actuar como un proveedor de libreta de direcciones host

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de host es un proveedor de la libreta de direcciones que incluye a los destinatarios de otros proveedores en sus contenedores y se basa en la implementación de los destinatarios por los demás proveedores para controlar parcialmente su mantenimiento. Un proveedor de host usa los identificadores de la plantilla de estos destinatarios externos para enlazar los datos para estos destinatarios al código en el proveedor extranjero. Este proceso de enlace se inicia cuando el proveedor recupera la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de un destinatario y lo pasa en una llamada a [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
  
Cuando las llamadas de proveedor **IMAPISupport::OpenTemplateID**, MAPI coincide con el **MAPIUID** dentro del identificador de plantilla con un **MAPIUID** registrados por un proveedor y llama al método [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) del proveedor. El proveedor externo puede devolver un puntero al objeto de propiedad de su proveedor, a su propia implementación de objeto (propiedad), o a una implementación que ajusta el objeto de su proveedor. El puntero devuelto se coloca en el contenido del parámetro _lppMAPIPropNew_ . 
  
Su proveedor puede elegir si desea llamar a **IMAPISupport::OpenTemplateID** con el conjunto de marca FILL_ENTRY o no. Establezca esta marca cuando se está creando el destinatario o cuando ha transcurrido mucho tiempo desde que el proveedor actualiza las propiedades del destinatario. Un uso común de la marca FILL_ENTRY consiste en mantener un destinatario en su proveedor sincronizado con el original. Implementar este tipo de programación de la sincronización mejora el rendimiento. 
  
 **Para mantener a un destinatario externo sincronizado**
  
1. Determinar un intervalo adecuado para las actualizaciones periódicas. 
    
2. Marca de tiempo de cada llamada a [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Evaluar si es necesario realizar una actualización completa en función de la cantidad de tiempo que ha caducado desde la última llamada. Si es necesaria una actualización completa, llame a **IMAPISupport::OpenTemplateID** con la marca FILL_ENTRY. Si no es necesario, no establezca la marca en la llamada. 
    
Cuando un cliente realiza una solicitud de una de las propiedades del destinatario copiada, su proveedor puede elegir si desea controlar la solicitud propio o utilizar el código proporcionado por el proveedor externo. Su proveedor puede esperar el proveedor extranjero para interceptar más, si no todas, las llamadas a **IMAPIProp** excepto [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Siempre se desvía una llamada a **OpenProperty** que solicita la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) a su proveedor.
  
 **Para obtener acceso a código de identificador de plantilla**
  
1. Abra al destinatario y llamar a su método [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si se produce un error de **GetProps** porque **PR_TEMPLATEID** no está disponible, el proveedor externo no admite un identificador de plantilla y código relacionado para este destinatario. El proveedor tendrá que utilizar su implementación del destinatario para todo el mantenimiento. 
    
2. Si se devuelve el identificador de plantilla de **GetProps**, pase lo y un puntero a la implementación de **IMAPIProp** del destinatario en una llamada al método **IMAPISupport::OpenTemplateID** . Establecer la marca FILL_ENTRY si la mayoría o todas las propiedades del destinatario necesitan ser actualizado, como en la hora de creación o si no han sido actualizados durante un tiempo. 
    
3. Si **OpenTemplateID** devuelve la externa implementación del proveedor **IMAPIProp** , devolver al cliente un puntero a esta implementación. 
    
4. Si **OpenTemplateID** devolver una implementación, normalmente debido a que el proveedor externo no está en el perfil, devolver al cliente un puntero a la implementación de **IMAPIProp** de su proveedor. El cliente debe ser capaz de trabajar con las propiedades del objeto con ninguna de las interfaces. 
    

