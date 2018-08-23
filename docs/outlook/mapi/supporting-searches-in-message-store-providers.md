---
title: Admitir búsquedas en proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f206623103f810b2868502aea7c6804cd306f022
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573197"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="a27a2-103">Admitir búsquedas en proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="a27a2-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="a27a2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a27a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a27a2-105">Con frecuencia, las aplicaciones cliente presentan algunos componentes de la interfaz de usuario dedicados a la búsqueda de mensajes en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a27a2-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="a27a2-106">Criterios de búsqueda se especifican en el [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) interfaz por medio de los métodos [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) y [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="a27a2-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="a27a2-107">Los clientes utilizan la propiedad de **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) del objeto de almacén de mensajes para identificar la carpeta raíz en el almacén de mensajes que contiene carpetas para los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a27a2-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="a27a2-108">La carpeta de resultados de búsqueda a menudo es una carpeta en el nivel superior del almacén de mensajes que no forma parte del árbol de carpetas IPM y, por lo tanto, oculto.</span><span class="sxs-lookup"><span data-stu-id="a27a2-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="a27a2-109">Si su proveedor de almacén de mensajes utiliza una carpeta de resultados de búsqueda permanente o crea uno cuando un cliente abre el identificador de entrada que se almacenan en la propiedad **PR_FINDER_ENTRYID** es un detalle de implementación.</span><span class="sxs-lookup"><span data-stu-id="a27a2-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="a27a2-110">Es algo más fácil de su proveedor de almacén de mensajes para usar una carpeta permanente que se crea cuando se crea el almacén de mensajes, ya que si lo hace por lo que evita la complejidad de comprobar el identificador de entrada siempre que se abre cualquier carpeta para ver si va a crear un carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a27a2-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="a27a2-111">Sin embargo, no todos los proveedores de almacén de mensajes pueden hacer; en particular, almacenes de mensaje de sólo lectura o que proporcionan una interfaz de MAPI para una base de datos heredado a menudo no se permiten o no puede crear una carpeta de resultados de búsqueda permanente en el mecanismo de almacenamiento subyacente.</span><span class="sxs-lookup"><span data-stu-id="a27a2-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a27a2-112">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a27a2-112">See also</span></span>



[<span data-ttu-id="a27a2-113">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="a27a2-113">Message Store Features</span></span>](message-store-features.md)

