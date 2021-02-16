---
title: Características necesarias para contenedores de libreta de direcciones
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
# <a name="required-features-for-address-book-containers"></a>Características necesarias para contenedores de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La mayoría de los proveedores de libretas de direcciones admiten al menos un contenedor, algunos de ellos modificables. Los contenedores de libreta de direcciones pueden proporcionar contenido y tablas de jerarquía, capacidades de búsqueda y resolución de nombres. Los contenedores modificables permiten la eliminación de entradas como usuarios de mensajería, listas de distribución u otros contenedores, así como la adición de entradas de entradas de otros contenedores o de plantillas de uso único.
  
En la tabla siguiente se describen las características necesarias para los proveedores de libretas de direcciones que tienen contenedores, modificables o de solo lectura, y cómo implementarlos.
  
|**Característica**|**Cómo implementar**|
|:-----|:-----|
|Obtener acceso a usuarios de mensajería  <br/> |Implemente [el método IABLogon::OpenEntry.](iablogon-openentry.md) Para obtener más información, vea [Abrir entradas de la libreta de direcciones.](opening-address-book-entries.md)  <br/> |
|Comparar usuarios de mensajería  <br/> |Implemente [el método IABLogon::CompareEntryIDs.](iablogon-compareentryids.md) Para obtener más información, vea [Comparar entradas de la libreta de direcciones.](comparing-address-book-entries.md)  <br/> |
|Crear usuarios de mensajería  <br/> |1. Proporcione una lista de plantillas de creación en una tabla de uso único mediante la compatibilidad con **la PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Para obtener más información, vea [Implementación de un contenedor One-Off tabla](implementing-a-container-one-off-table.md).  <br/> 2. Implemente el [método IABContainer::CreateEntry.](iabcontainer-createentry.md) Para obtener más información, vea [Agregar entradas de la libreta de direcciones.](adding-address-book-entries.md)  <br/> |
|Copiar usuarios de mensajería  <br/> |Implementa el [método IABContainer::CopyEntries.](iabcontainer-copyentries.md) Para obtener más información, [vea Copiar entradas de la libreta de direcciones.](copying-address-book-entries.md)  <br/> |
|Quitar usuarios de mensajería  <br/> |Implementa el [método IABContainer::D eleteEntries.](iabcontainer-deleteentries.md) Para obtener más información, vea [Quitar entradas de la libreta de direcciones.](removing-address-book-entries.md)  <br/> |
|Proporcionar información resumida sobre los usuarios de mensajería  <br/> |Admite la propiedad **contenedora PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Tablas de contenido](contents-tables.md).  <br/> |
|Proporcionar información detallada sobre los usuarios de mensajería  <br/> |Admite la **propiedad PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) en los usuarios de mensajería y las listas de distribución. Para obtener más información, vea [Mostrar información de destinatarios](displaying-recipient-information.md) y Tablas para [mostrar.](display-tables.md)  <br/> |
|Proporcionar información detallada sobre un contenedor  <br/> |Admite la **PR_DETAILS_TABLE** propiedad en el contenedor. Para obtener más información, vea [Mostrar información de destinatarios](displaying-recipient-information.md) y Tablas para [mostrar.](display-tables.md)  <br/> |
|Proporcionar una lista jerárquica de contenedores  <br/> |Admite la propiedad **contenedora PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Para obtener más información, vea [Tablas de jerarquía.](hierarchy-tables.md)  <br/> |
|Compatibilidad con propiedades de usuario de mensajería  <br/> |Implemente [la interfaz IMailUser : IMAPIProp.](imailuserimapiprop.md)  <br/> |
|Resolver nombres ambiguos  <br/> | Admite la **restricción PR_ANR** propiedad ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  Opcionalmente, implementa [el método IABContainer::ResolveNames.](iabcontainer-resolvenames.md) For more information, see [Implementaci�n de la resoluci�n de nombres](implementing-name-resolution.md).  <br/> |
   

