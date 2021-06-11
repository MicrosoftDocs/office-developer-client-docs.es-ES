---
title: Agregar entradas de libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421343"
---
# <a name="adding-address-book-entries"></a>Agregar entradas de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para agregar un usuario de mensajería o una lista de distribución a un contenedor, un cliente llama a [IAddrBook::NewEntry](iaddrbook-newentry.md) o un proveedor llama a [IMAPISupport::NewEntry con](imapisupport-newentry.md) el identificador de entrada del contenedor de destino en el parámetro _lpEIDContainer._ MAPI a su vez llama al método [IABContainer::CreateEntry](iabcontainer-createentry.md) del contenedor para crear la entrada con una plantilla de uso único desde una tabla de uso único. Una plantilla de uso único permite al cliente crear un nuevo destinatario de un tipo determinado. La mayoría de los campos son editables. La plantilla a la que apunta el parámetro  _lpEntryID_ puede ser una que el proveedor proporciona o puede ser una plantilla de un proveedor externo, si el proveedor admite plantillas extranjeras. Las implementaciones de **CreateEntry** para proveedores que pueden crear destinatarios a partir de una plantilla externa siempre son más complejas que las implementaciones para proveedores que no pueden. 
  
 **Para implementar IABContainer::CreateEntry**
  
1. Determine el tipo de identificador de entrada especificado por el _parámetro lpEntryID._ 
    
2. Si el identificador de entrada representa una plantilla para un usuario de mensajería, una lista de distribución o un contenedor de libreta de direcciones propiedad del proveedor:
    
1. Cree e inicialice el objeto adecuado. El proveedor puede establecer algunas propiedades iniciales si lo desea. Estas propiedades dependen del tipo de destinatario que se cree. 
    
2. Devuelve un puntero a la implementación del objeto en el contenido del parámetro _lppMAPIPropEntry._ 
    
3. Si el identificador de entrada representa una plantilla para un proveedor externo:
    
1. Llame [a IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir el objeto externo. 
    
2. Llame al método [IMAPIProp::GetProps del](imapiprop-getprops.md) objeto, pasando NULL para la matriz de etiquetas de propiedad, para recuperar sus propiedades. 
    
3. Edite la matriz de valores de propiedad devuelta de **GetProps** cambiando la etiqueta de propiedad a PR_NULL para todas las propiedades que no se aplicarán al nuevo objeto y no se deben transferir. 
    
4. Cree un identificador de entrada para el nuevo objeto. 
    
5. Cree un nuevo objeto del tipo adecuado, ya sea el usuario de mensajería o la lista de distribución.
    
6. Inicialice el nuevo objeto estableciendo las propiedades predeterminadas.
    
7. Compruebe si el objeto externo admite la **propiedad PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). 
    
8. Si el objeto externo admite **PR_TEMPLATEID**, llame a [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para recuperar una interfaz de objeto de propiedad del proveedor externo y establezca el contenido del parámetro  _lppMAPIPropEntry_ en la implementación del objeto de propiedad externa. 
    
9. Si el objeto externo no admite PR_TEMPLATEID **,** establezca el contenido del parámetro  _lppMAPIPropEntry_ en la implementación del nuevo objeto por parte del proveedor. 
    
10. Llame al [método IMAPIProp::SetProps](imapiprop-setprops.md) del objeto al que apunta el parámetro  _lppMAPIPropEntry_ para establecer las propiedades apropiadas del objeto externo. 
    

