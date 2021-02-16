---
title: Buscar en la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d40419291f4b09c5880a769ce231015511e8f269
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424374"
---
# <a name="searching-the-address-book"></a>Buscar en la libreta de direcciones

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI permite a los proveedores de libreta de direcciones implementar dos niveles de funcionalidad de b�squeda:
  
- Nivel básico que coincide con un nombre especificado con **la propiedad PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de las entradas de la libreta de direcciones. Este nivel permite a los usuarios, por ejemplo, para ver listas de distribuci�n cuyos nombres empiecen por noroeste o buscar usuarios de mensajer�a individuales cuyo apellido sea marr�n.
    
- Un nivel avanzado que se encuentra en las propiedades que no sean **PR_DISPLAY_NAME**. Este nivel permite a los usuarios, por ejemplo, para restringir a�n m�s sus b�squedas y buscar usuarios denominados Brown con un tipo de direcci�n concreto de mensajer�a.
    
Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature. To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches. 
  
In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). You can also request that the user be prompted for search criteria before a container's contents table is displayed. Para elegir esta opción, establece la marca AB_FIND_ON_OPEN de la propiedad PR_CONTAINER_FLAGS **del** contenedor ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method. Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>Para realizar una b�squeda b�sica en un contenedor de libreta de direcciones
  
1. Call the container's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table. 
    
2. Elija una t�cnica de b�squeda que satisfaga sus necesidades. Las opciones son:
    
   - [IMAPITable::FindRow](imapitable-findrow.md) to locate a specific row in the table. 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md) to order rows in the table. 
    
   - [IMAPITable:: Restrict](imapitable-restrict.md) to limit the table view. 
    
   - Restricción de propiedad mediante **la PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para resolver nombres ambiguos. Llamar a **IMAPITable:: Restrict** para imponer esta restricci�n. 
    
   - [IABContainer::ResolveNames](iabcontainer-resolvenames.md) to resolve ambiguous names. 
    
3. Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve any rows that meet your applied search criteria. **QueryRows** can return zero or more matching rows. 
    
Los m�todos **FindRow**, **SortTable** y **Restrict** son m�todos de tabla que est�n disponibles para cualquier tabla que se pueden crear, ya sea un cliente o un proveedor de servicios. La **restricción de la propiedad PR \_ ANR** y el método **IABContainer::ResolveNames** son específicos de los proveedores de libretas de direcciones y se usan para resolver nombres ambiguos. Nombres ambiguos son entradas en una lista de destinatarios que no tienen una propiedad de **PR_ENTRYID** asociada a ellos. 
  
La **restricción \_ PR ANR** invoca un algoritmo que separa una cadena de caracteres en palabras y las encuentra con información en la libreta de direcciones mediante la coincidencia de prefijos. The information used for the matching depends on the address book provider. All address book providers are required to support the **PR_ANR** restriction for their address book containers. For more information, see [Implementaci�n de la resoluci�n de nombres](implementing-name-resolution.md).
  
**IABContainer::ResolveNames** realiza **PR_ANR** restricci�n de procesamiento en varios nombres sin necesidad de tabla de contenido del contenedor est� abierto. Llamar **a ResolveNames una** vez para resolver varios nombres puede ser mucho más rápido que invocar varias veces una restricción DE PR **\_ ANR.** Sin embargo, los proveedores de libreta de direcciones no deben admitir **ResolveNames**.
  

