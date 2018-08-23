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
ms.openlocfilehash: d5b2aa2830e2721b9f895b22df12c9d712188625
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590137"
---
# <a name="adding-address-book-entries"></a>Agregar entradas de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para agregar un usuario de mensajería o lista de distribución a un contenedor, un [IAddrBook::NewEntry](iaddrbook-newentry.md) las llamadas del cliente o un proveedor llama a [IMAPISupport::NewEntry](imapisupport-newentry.md) con el identificador de entrada del contenedor de destino en el parámetro _lpEIDContainer_ . MAPI a su vez llama al método [IABContainer::CreateEntry](iabcontainer-createentry.md) del contenedor para crear la entrada de uso de una plantilla de uso único de una tabla de uso único. Una plantilla de uso único permite que el cliente crear a un nuevo destinatario de un tipo determinado. La mayoría de los campos es editable. La plantilla indicada por el parámetro _lpEntryID_ es posible que uno que suministra el proveedor o podría ser una plantilla de un proveedor externo, si su proveedor admite plantillas externas. Las implementaciones de **CreateEntry** para los proveedores que se pueden crear destinatarios desde una plantilla externa siempre son más complejas que las implementaciones de los proveedores que no se pueden. 
  
 **Para implementar IABContainer::CreateEntry**
  
1. Determinar el tipo de identificador de entrada especificado por el parámetro _lpEntryID_ . 
    
2. Si el identificador de entrada representa una plantilla para un usuario de mensajería, la lista de distribución o el contenedor de la libreta de direcciones que pertenecen a su proveedor de:
    
1. Crear e inicializar el objeto correspondiente. El proveedor puede establecer algunas propiedades iniciales si así lo desea. Estas propiedades dependen del tipo de destinatario que se está creando. 
    
2. Devolver un puntero a la implementación del objeto en el contenido del parámetro _lppMAPIPropEntry_ . 
    
3. Si el identificador de entrada representa una plantilla para un proveedor externo:
    
1. Llame a [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir el objeto externo. 
    
2. Llame al método del objeto [IMAPIProp::GetProps](imapiprop-getprops.md) , pasando NULL para la matriz de etiqueta de propiedad, para recuperar sus propiedades. 
    
3. Editar la matriz de valores de propiedad devuelta desde **GetProps** cambiando la etiqueta de propiedad a PR_NULL para todas las propiedades que no se aplicarán al nuevo objeto y no se transferirá. 
    
4. Crear un identificador de entrada para el nuevo objeto. 
    
5. Crear un nuevo objeto de la adecuada escriba puede ser mensajería usuario o lista de distribución.
    
6. Inicializar el nuevo objeto estableciendo las propiedades predeterminadas.
    
7. Compruebe si el objeto externo es compatible con la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). 
    
8. Si el objeto externo admite **PR_TEMPLATEID**, llame a [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para recuperar una interfaz de objeto de la propiedad del proveedor externo y establecer el contenido del parámetro _lppMAPIPropEntry_ para la propiedad foreign implementación de objeto. 
    
9. Si el objeto externo no admite **PR_TEMPLATEID**, establezca el contenido del parámetro _lppMAPIPropEntry_ en la implementación de su proveedor del nuevo objeto. 
    
10. Llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) del objeto indicado por el parámetro _lppMAPIPropEntry_ para establecer las propiedades adecuadas desde el objeto externo. 
    

