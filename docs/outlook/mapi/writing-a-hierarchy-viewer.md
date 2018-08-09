---
title: Escribir un visor de jerarquía
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0286696707d268867a5536ef345d0af7909918dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820995"
---
# <a name="writing-a-hierarchy-viewer"></a>Escribir un visor de jerarquía

  
  
**Hace referencia a**: Outlook 
  
Un visor de jerarquía es un componente de la interfaz de usuario que se usa para mostrar la carpeta y la dirección tablas de jerarquía del contenedor de libro. Visores de jerarquía pueden mostrar a los miembros de la jerarquía en diferentes niveles, expandir y cada nivel de petición de contratación.
  
La propiedad container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controla el nivel en el que se muestra un miembro de la jerarquía. Las entradas que representan los contenedores de la libreta de direcciones de nivel superior o carpetas tienen su propiedad **PR_DEPTH** establece en cero. El valor de esta propiedad se incrementa secuencialmente para las entradas en los niveles de secuenciales. Es decir, cuando un usuario selecciona un contenedor de nivel superior para expandir, mostrar todos los contenedores con **PR_DEPTH** establecen en 1. Cuando un usuario expande uno de estos subcontenedores, mostrar los contenedores con conjunto **PR_DEPTH** a 2 y así sucesivamente. 
  
Visores de jerarquía admiten un intervalo de profundidad diferente. Puede limitar el Visor para sólo uno o dos niveles o puede admitir varios niveles, si mostrar una jerarquía amplia es una prioridad. 
  
La libreta de direcciones proporciona un visor de jerarquía de los contenedores de nivel superior en la libreta de direcciones. 
  
 **Para obtener acceso a la tabla de jerarquía de la libreta de direcciones**
  
1. Llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md), pasando un identificador de entrada null, para abrir el contenedor de raíz de la libreta de direcciones.
    
2. Llamar al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) del contenedor raíz para obtener acceso a la tabla de jerarquía de la libreta de direcciones MAPI. 
    
 **Para obtener acceso a la tabla de jerarquía del almacén de mensajes predeterminado**
  
1. Llame a [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para obtener acceso a la tabla de almacén de mensajes. 
    
2. Crear una restricción de uso de la estructura [SPropertyRestriction](spropertyrestriction.md) para limitar la tabla a sólo las filas que tienen un conjunto de propiedades **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) en TRUE. 
    
3. Llamar a [IMAPITable:: FindRow](imapitable-findrow.md), pasando el **SPropertyRestriction**, para buscar la fila que representa el almacén de mensajes predeterminado. 
    
4. Llame a [IMAPISession::OpenEntry](imapisession-openentry.md), pasando la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la fila del almacén de mensajes de forma predeterminada en la tabla de almacén de mensajes.
    
5. Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
6. Llamar al método [IMsgStore::OpenEntry](imsgstore-openentry.md) del almacén de mensajes, pasando la propiedad **PR_IPM_SUBTREE_ENTRYID** , para abrir la carpeta raíz del subárbol IPM del almacén de mensajes. 
    
7. Llamar al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) de la carpeta raíz IPM para tener acceso a su tabla de jerarquía. 
    

