---
title: Características necesarias para los contenedores de la libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5eeaa9a8c1965954ad2eb0a6bfd2a174a355f10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820521"
---
# <a name="required-features-for-address-book-containers"></a>Características necesarias para los contenedores de la libreta de direcciones

  
  
**Se aplica a**: Outlook 
  
La mayoría de los proveedores de la libreta de direcciones compatible con al menos un contenedor, algunos de ellos modificable. Contenedores de la libreta de direcciones pueden suministrar contenido y las tablas de jerarquía, las capacidades de búsqueda y resolución de nombres. Contenedores modificables permiten la eliminación de entradas, como los usuarios, las listas de distribución, u otros contenedores y la adición de entradas de las entradas de otros contenedores o de plantillas de uso único de mensajería.
  
En la siguiente tabla se describe las características que son necesarias de los proveedores de la libreta de direcciones que tienen contenedores, modificables o de sólo lectura, y cómo implementarlos.
  
|**Característica**|**Cómo implementar**|
|:-----|:-----|
|Obtener acceso a los usuarios de mensajería  <br/> |Implemente el método [IABLogon::OpenEntry](iablogon-openentry.md) . Para obtener más información, vea las [Entradas de la libreta de direcciones de apertura](opening-address-book-entries.md).  <br/> |
|Comparación de los usuarios de mensajería  <br/> |Implemente el método [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) . Para obtener más información, vea [Comparación de entradas de la libreta de direcciones](comparing-address-book-entries.md).  <br/> |
|Crear usuarios de mensajería  <br/> |1. compatible con la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para proporcionar una lista de plantillas de creación de una tabla de uso único. Para obtener más información, vea [implementación de una tabla de uso único de contenedor](implementing-a-container-one-off-table.md).  <br/> 2. implemente el método [IABContainer::CreateEntry](iabcontainer-createentry.md) . Para obtener más información, vea [Agregar entradas de la libreta de direcciones](adding-address-book-entries.md).  <br/> |
|Copie los usuarios de mensajería  <br/> |Implemente el método [IABContainer::CopyEntries](iabcontainer-copyentries.md) . Para obtener más información, vea [Copiar entradas de la libreta de direcciones](copying-address-book-entries.md).  <br/> |
|Quitar usuarios de mensajería  <br/> |Implemente el método [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) . Para obtener más información, vea [Quitar entradas de la libreta de direcciones](removing-address-book-entries.md).  <br/> |
|Proporcionar información de resumen acerca de los usuarios de mensajería  <br/> |Admite la propiedad container **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Tablas de contenido](contents-tables.md).  <br/> |
|Proporcionan información detallada acerca de los usuarios de mensajería  <br/> |Admite la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) en los usuarios y las listas de distribución de mensajería. Para obtener más información, vea [Mostrar información de destinatario](displaying-recipient-information.md) y [Tablas para mostrar](display-tables.md).  <br/> |
|Proporcionan información detallada acerca de un contenedor  <br/> |Admite la propiedad **PR_DETAILS_TABLE** en el contenedor. Para obtener más información, vea [Mostrar información de destinatario](displaying-recipient-information.md) y [Tablas para mostrar](display-tables.md).  <br/> |
|Proporcionar una lista jerárquica de contenedores  <br/> |Admite la propiedad container **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Para obtener más información, vea [Las tablas de jerarquía](hierarchy-tables.md).  <br/> |
|Compatibilidad con las propiedades de usuario de mensajería  <br/> |Implementar el [IMailUser: IMAPIProp](imailuserimapiprop.md) interfaz.  <br/> |
|Resolver nombres ambiguos  <br/> | Admite la restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  Opcionalmente, implemente el método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . For more information, see [Implementaci�n de la resoluci�n de nombres](implementing-name-resolution.md).  <br/> |
   

