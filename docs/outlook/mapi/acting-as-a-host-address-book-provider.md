---
title: Actuar como un proveedor de libreta de direcciones de host
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 202d4b4391de7553e39e50dc527df5502ebcefb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331272"
---
# <a name="acting-as-a-host-address-book-provider"></a>Actuar como un proveedor de libreta de direcciones de host

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de host es un proveedor de libretas de direcciones que incluye destinatarios de otros proveedores en sus contenedores y depende de la implementación de los destinatarios por parte de los otros proveedores para controlar su mantenimiento de forma parcial. Un proveedor de host usa los identificadores de plantilla de estos destinatarios externos para enlazar los datos de estos destinatarios al código del proveedor externo. Este proceso de enlace se inicia cuando el proveedor recupera la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de un destinatario y la pasa en una llamada a [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md). 
  
Cuando el proveedor llama a **IMAPISupport:: OpenTemplateID**, MAPI hace coincidir el **MAPIUID** dentro del identificador de la plantilla con un **MAPIUID** registrado por un proveedor y llama al método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) del proveedor. El proveedor externo puede devolver un puntero al objeto Property del proveedor, a su propia implementación de objeto Property o a una implementación que contenga el objeto de proveedor. El puntero devuelto se coloca en el contenido del parámetro _lppMAPIPropNew_ . 
  
El proveedor puede elegir si desea llamar a **IMAPISupport:: OpenTemplateID** con la marca FILL_ENTRY establecida. Establezca este indicador cuando se cree el destinatario o cuando haya transcurrido mucho tiempo desde que el proveedor haya actualizado las propiedades del destinatario. Un uso común de la marca FILL_ENTRY es mantener sincronizado un destinatario del proveedor con el original. La implementación de este tipo de programación de sincronización mejora el rendimiento. 
  
 **Para mantener sincronizado un destinatario externo**
  
1. DeTermine un intervalo adecuado para las actualizaciones periódicas. 
    
2. Marca de hora cada llamada a [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Evalúe si es necesario o no realizar una actualización completa en función de la cantidad de tiempo que ha expirado desde la última llamada. Si se necesita una actualización completa, llame a **IMAPISupport:: OpenTemplateID** con la marca FILL_ENTRY. Si no es necesario, no establezca la marca en la llamada. 
    
Cuando un cliente realiza una solicitud para una de las propiedades del destinatario copiado, el proveedor puede elegir si desea controlar la solicitud o usar el código proporcionado por el proveedor externo. El proveedor puede esperar que el proveedor externo intercepte la mayoría de las llamadas a **IMAPIProp** excepto para [IMAPIProp:: OpenProperty](imapiprop-openproperty.md). Siempre se reenvía a su proveedor una llamada a **OpenProperty** que solicita la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).
  
 **Para tener acceso al código de identificador de plantilla**
  
1. Abra el destinatario y llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) para recuperar la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si **GetProps** produce un error porque **PR_TEMPLATEID** no está disponible, el proveedor externo no admite un identificador de plantilla y código relacionado para este destinatario. El proveedor deberá usar su implementación del destinatario para todo el mantenimiento. 
    
2. Si el identificador de plantilla se devuelve desde **GetProps**, páselo y un puntero a la implementación de **IMAPIProp** del destinatario en una llamada al método **IMAPISupport:: OpenTemplateID** . Establezca la marca FILL_ENTRY si la mayoría o todas las propiedades del destinatario deben actualizarse, como en el momento de la creación o si no se han actualizado durante un tiempo. 
    
3. Si **OpenTemplateID** devuelve la implementación de **IMAPIProp** del proveedor externo, devuelva al cliente un puntero a esta implementación. 
    
4. Si **OpenTemplateID** no devuelve una implementación, normalmente porque el proveedor externo no está en el perfil, regrese al cliente un puntero a la implementación de **IMAPIProp** del proveedor. El cliente debe poder trabajar con las propiedades del objeto mediante cualquiera de las interfaces. 
    

