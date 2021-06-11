---
title: Escritura de un visor de jerarquía
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421133"
---
# <a name="writing-a-hierarchy-viewer"></a>Escritura de un visor de jerarquía

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un visor de jerarquía es un componente de interfaz de usuario que se usa para mostrar tablas de jerarquía de contenedor de carpetas y libretas de direcciones. Los visores de jerarquía pueden mostrar miembros de la jerarquía en diferentes niveles, expandiendo y contrayendo cada nivel a petición.
  
La propiedad container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controla el nivel en el que se muestra un miembro de jerarquía. Las entradas que representan carpetas o contenedores de libreta de direcciones de nivel superior **tienen su PR_DEPTH** propiedad establecida en cero. El valor de esta propiedad se incrementa secuencialmente para las entradas en niveles secuenciales. Es decir, cuando un usuario selecciona un contenedor de nivel superior para expandirlo, muestre todos los contenedores **con PR_DEPTH** establecido en 1. Cuando un usuario expande uno de estos subcontenedores, muestra los contenedores **con PR_DEPTH** establecido en 2, y así sucesivamente. 
  
Los visores de jerarquía admiten un rango diferente de profundidades. Puede limitar el visor a solo uno o dos niveles o puede admitir varios niveles, si mostrar una jerarquía expansiva es una prioridad. 
  
La libreta de direcciones proporciona un visor de jerarquía para los contenedores de nivel superior de la libreta de direcciones. 
  
 **Para obtener acceso a la tabla de jerarquía de libreta de direcciones**
  
1. Llama [a IAddrBook::OpenEntry](iaddrbook-openentry.md), pasando un identificador de entrada nulo, para abrir el contenedor raíz de la libreta de direcciones.
    
2. Llame al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) del contenedor raíz para obtener acceso a la tabla de jerarquía de la libreta de direcciones MAPI. 
    
 **Para obtener acceso a la tabla de jerarquía del almacén de mensajes predeterminada**
  
1. Llame [a IMAPISession::GetMsgStoresTable para](imapisession-getmsgstorestable.md) obtener acceso a la tabla de almacén de mensajes. 
    
2. Cree una restricción mediante la estructura [SPropertyRestriction](spropertyrestriction.md) para limitar la tabla solo a las filas que tienen una propiedad **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) establecida en TRUE. 
    
3. Llame [a IMAPITable::FindRow](imapitable-findrow.md), pasando la **SPropertyRestriction**, para buscar la fila que representa el almacén de mensajes predeterminado. 
    
4. Llame [a IMAPISession::OpenEntry](imapisession-openentry.md), pasando la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la fila del almacén de mensajes predeterminada en la tabla del almacén de mensajes.
    
5. Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
6. Llama al método [IMsgStore::OpenEntry](imsgstore-openentry.md) del almacén de mensajes, pasando la propiedad **PR_IPM_SUBTREE_ENTRYID, para** abrir la carpeta raíz del subárbol IPM del almacén de mensajes. 
    
7. Llame al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) de la carpeta raíz IPM para obtener acceso a su tabla de jerarquía. 
    

