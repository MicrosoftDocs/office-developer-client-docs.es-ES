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
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349591"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="57cad-103">Admitir búsquedas en proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="57cad-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="57cad-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57cad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57cad-105">Las aplicaciones cliente con frecuencia tienen algunos componentes de la interfaz de usuario dedicados a la búsqueda de mensajes en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="57cad-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="57cad-106">Los criterios de búsqueda se especifican en la interfaz [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) por medio de los métodos [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) y [IMAPIContainer:: GetSearchCriteria](imapicontainer-getsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="57cad-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="57cad-107">Los clientes usan la propiedad **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) del objeto de almacén de mensajes para identificar la carpeta raíz del almacén de mensajes que contiene carpetas para los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="57cad-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="57cad-108">La carpeta de resultados de búsqueda suele ser una carpeta en el nivel superior del almacén de mensajes que no forma parte del árbol de carpetas IPM y que, por lo tanto, está oculta.</span><span class="sxs-lookup"><span data-stu-id="57cad-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="57cad-109">Si su proveedor de almacenamiento de mensajes utiliza una carpeta de resultados de búsqueda permanente o crea una cuando un cliente abre el identificador de entrada almacenado en la propiedad **PR_FINDER_ENTRYID** es un detalle de implementación.</span><span class="sxs-lookup"><span data-stu-id="57cad-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="57cad-110">Es algo más sencillo para su proveedor de almacenamiento de mensajes usar una carpeta permanente que se crea cuando se crea el almacén de mensajes, porque al hacerlo se evita la complicación de comprobar el identificador de entrada siempre que se abra cualquier carpeta para ver si se crea una carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="57cad-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="57cad-111">Sin embargo, no todos los proveedores de almacenamiento de mensajes pueden hacerlo; en concreto, los almacenes de mensajes de solo lectura o los almacenes que proporcionan una interfaz MAPI a una base de datos heredada a menudo no se permiten o no pueden crear una carpeta de resultados de búsqueda permanente en el mecanismo de almacenamiento subyacente.</span><span class="sxs-lookup"><span data-stu-id="57cad-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="57cad-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="57cad-112">See also</span></span>



[<span data-ttu-id="57cad-113">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="57cad-113">Message Store Features</span></span>](message-store-features.md)

