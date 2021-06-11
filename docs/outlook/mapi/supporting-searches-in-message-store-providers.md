---
title: Admitir búsquedas en proveedores de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425389"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="fa2ae-103">Admitir búsquedas en proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="fa2ae-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="fa2ae-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa2ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa2ae-105">Las aplicaciones cliente suelen tener algunos componentes de interfaz de usuario dedicados a buscar mensajes en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="fa2ae-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="fa2ae-106">Los criterios de búsqueda se especifican en la interfaz [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) mediante los métodos [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) e [IMAPIContainer::GetSearchCriteria.](imapicontainer-getsearchcriteria.md)</span><span class="sxs-lookup"><span data-stu-id="fa2ae-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="fa2ae-107">Los clientes usan la propiedad PR_FINDER_ENTRYID **del** objeto de almacén de mensajes ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) para identificar la carpeta raíz del almacén de mensajes que contiene carpetas para los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fa2ae-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="fa2ae-108">La carpeta de resultados de búsqueda suele ser una carpeta en el nivel superior del almacén de mensajes que no forma parte del árbol de carpetas IPM y, por lo tanto, está oculta.</span><span class="sxs-lookup"><span data-stu-id="fa2ae-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="fa2ae-109">Si el proveedor del almacén de mensajes usa una carpeta de resultados de búsqueda permanente o crea una cuando un cliente abre el identificador de entrada almacenado en la **propiedad PR_FINDER_ENTRYID** es un detalle de implementación.</span><span class="sxs-lookup"><span data-stu-id="fa2ae-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="fa2ae-110">Es algo más fácil para el proveedor del almacén de mensajes usar una carpeta permanente que se crea cuando se crea el almacén de mensajes, ya que hacerlo evita la complicación de comprobar el identificador de entrada siempre que se abra cualquier carpeta para ver si se va a crear una carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fa2ae-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="fa2ae-111">Sin embargo, no todos los proveedores de almacén de mensajes pueden hacerlo; En particular, los almacenes o almacenes de mensajes de solo lectura que proporcionan una interfaz MAPI a una base de datos heredada a menudo no están permitidos o no pueden crear una carpeta de resultados de búsqueda permanente en el mecanismo de almacenamiento subyacente.</span><span class="sxs-lookup"><span data-stu-id="fa2ae-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa2ae-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa2ae-112">See also</span></span>



[<span data-ttu-id="fa2ae-113">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="fa2ae-113">Message Store Features</span></span>](message-store-features.md)

