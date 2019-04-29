---
title: Características necesarias para los contenedores de la libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: abdbd9030e0ea053d39b49ecc76a78821be9df82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439684"
---
# <a name="required-features-for-address-book-containers"></a>Características necesarias para los contenedores de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La mayoría de los proveedores de libreta de direcciones admite al menos un contenedor, algunos de ellos modificables. Los contenedores de la libreta de direcciones pueden proporcionar tablas de contenido y jerarquía, capacidades de búsqueda y resolución de nombres. Los contenedores modificables permiten la eliminación de entradas como usuarios de mensajería, listas de distribución u otros contenedores y la adición de entradas de entradas de otros contenedores o de plantillas de un solo uso.
  
En la tabla siguiente se describen las características que son necesarias para los proveedores de libreta de direcciones que tienen contenedores, modificables o de solo lectura, y cómo se implementan.
  
|**Característica**|**Cómo implementar**|
|:-----|:-----|
|Acceso a usuarios de mensajería  <br/> |Implemente el método [IABLogon:: OpenEntry](iablogon-openentry.md) . Para obtener más información, consulte [abrir entradas](opening-address-book-entries.md)de la libreta de direcciones.  <br/> |
|Comparar usuarios de mensajería  <br/> |Implemente el método [IABLogon:: CompareEntryIDs](iablogon-compareentryids.md) . Para obtener más información, consulte [comparar entradas](comparing-address-book-entries.md)de la libreta de direcciones.  <br/> |
|Crear usuarios de mensajería  <br/> |1. proporcionar una lista de plantillas de creación en una tabla de uso único admitiendo la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Para obtener más información, vea [implementar una tabla de un contenedor de un solo uso](implementing-a-container-one-off-table.md).  <br/> 2. implemente el método [IABContainer:: CreateEntry](iabcontainer-createentry.md) . Para obtener más información, vea [Agregar entradas](adding-address-book-entries.md)de la libreta de direcciones.  <br/> |
|Copiar usuarios de mensajería  <br/> |Implemente el método [IABContainer:: CopyEntries](iabcontainer-copyentries.md) . Para obtener más información, consulte copia de entradas de la [Libreta de direcciones](copying-address-book-entries.md).  <br/> |
|Quitar usuarios de mensajería  <br/> |Implemente el método [IABContainer::D eleteentries](iabcontainer-deleteentries.md) . Para obtener más información, vea [quitar entradas](removing-address-book-entries.md)de la libreta de direcciones.  <br/> |
|Proporcionar información de resumen sobre los usuarios de mensajería  <br/> |Admitir la propiedad de contenedor **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Tablas de contenido](contents-tables.md).  <br/> |
|Proporcionar información detallada sobre los usuarios de mensajería  <br/> |Admitir la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) en los usuarios y las listas de distribución de mensajería. Para obtener más información, vea [Mostrar información](displaying-recipient-information.md) de destinatarios y [Mostrar tablas](display-tables.md).  <br/> |
|Proporcionar información detallada sobre un contenedor  <br/> |Admite la propiedad **PR_DETAILS_TABLE** del contenedor. Para obtener más información, vea [Mostrar información](displaying-recipient-information.md) de destinatarios y [Mostrar tablas](display-tables.md).  <br/> |
|Proporcionar una lista jerárquica de contenedores  <br/> |Admitir la propiedad de contenedor **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Para obtener más información, vea [tablas](hierarchy-tables.md)de jerarquías.  <br/> |
|Compatibilidad con propiedades de usuario de mensajería  <br/> |Implemente la interfaz [IMailUser: IMAPIProp](imailuserimapiprop.md) .  <br/> |
|Resolución de nombres ambiguos  <br/> | Admite la restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  Opcionalmente, implemente el método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . For more information, see [Implementaci�n de la resoluci�n de nombres](implementing-name-resolution.md).  <br/> |
   

