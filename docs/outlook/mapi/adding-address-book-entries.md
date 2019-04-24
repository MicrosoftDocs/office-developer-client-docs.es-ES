---
title: Agregar entradas de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331881"
---
# <a name="adding-address-book-entries"></a>Agregar entradas de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para agregar un usuario de mensajería o una lista de distribución a un contenedor, un cliente llama a [IAddrBook:: NEWENTRY](iaddrbook-newentry.md) o un proveedor llama a [IMAPISupport:: NEWENTRY](imapisupport-newentry.md) con el identificador de entrada del contenedor de destino en el parámetro _lpEIDContainer_ . MAPI a su vez llama al método [IABContainer:: CreateEntry](iabcontainer-createentry.md) del contenedor para crear la entrada usando una plantilla de uso único en una tabla de uso único. Una plantilla de uso único permite al cliente crear un nuevo destinatario de un tipo determinado. La mayoría de los campos son editables. La plantilla a la que señala el parámetro _lpEntryID_ puede ser una plantilla suministrada por el proveedor o puede ser una plantilla de un proveedor externo, si el proveedor admite plantillas externas. Las implementaciones de **CreateEntry** para proveedores que pueden crear destinatarios a partir de una plantilla externa son siempre más complejas que las implementaciones para los proveedores que no pueden. 
  
 **Para implementar IABContainer:: CreateEntry**
  
1. DeTermine el tipo de identificador de entrada especificado por el parámetro _lpEntryID_ . 
    
2. Si el identificador de entrada representa una plantilla para un usuario de mensajería, una lista de distribución o un contenedor de libretas de direcciones que pertenece al proveedor:
    
1. Cree e inicialice el objeto correspondiente. El proveedor puede establecer algunas propiedades iniciales si así lo desea. Estas propiedades dependen del tipo de destinatario que se va a crear. 
    
2. Devolver un puntero a la implementación del objeto en el contenido del parámetro _lppMAPIPropEntry_ . 
    
3. Si el identificador de entrada representa una plantilla para un proveedor externo:
    
1. Llame a [IMAPISupport:: OpenEntry](imapisupport-openentry.md) para abrir el objeto externo. 
    
2. Llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del objeto, pasando null para la matriz de etiquetas de propiedad, para recuperar sus propiedades. 
    
3. Edite la matriz de valores de propiedad devuelta desde **GetProps** cambiando la etiqueta de propiedad a PR_NULL para todas las propiedades que no se aplicarán al nuevo objeto y no deben transferirse. 
    
4. Cree un identificador de entrada para el objeto nuevo. 
    
5. Cree un nuevo objeto del tipo apropiado, ya sea usuario de mensajería o lista de distribución.
    
6. Inicialice el nuevo objeto estableciendo las propiedades predeterminadas.
    
7. Compruebe si el objeto externo admite o no la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). 
    
8. Si el objeto externo admite **PR_TEMPLATEID**, llame a [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) para recuperar una interfaz de objeto de propiedad del proveedor externo y establecer el contenido del parámetro _lppMAPIPropEntry_ en la propiedad Foreign. implementación de objetos. 
    
9. Si el objeto externo no es compatible con **PR_TEMPLATEID**, establezca el contenido del parámetro _lppMAPIPropEntry_ en la implementación del proveedor del nuevo objeto. 
    
10. Llame al método [IMAPIProp:: SetProps](imapiprop-setprops.md) del objeto al que señala el parámetro _lppMAPIPropEntry_ para establecer las propiedades apropiadas desde el objeto externo. 
    

