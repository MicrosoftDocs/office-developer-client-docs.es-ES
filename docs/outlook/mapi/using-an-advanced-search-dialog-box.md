---
title: Usar un cuadro de diálogo de búsqueda avanzada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3c27b859f6d056d3b9a98bd4d71db8e500dff696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820955"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="16846-103">Usar un cuadro de diálogo de búsqueda avanzada</span><span class="sxs-lookup"><span data-stu-id="16846-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="16846-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16846-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16846-105">Algunos contenedores de la libreta de direcciones compatible con una capacidad de búsqueda avanzada que permite a los clientes buscar en las propiedades que no sean **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="16846-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="16846-106">Contenedores de libretas de direcciones que admiten búsquedas avanzadas tienen una propiedad de objeto de contenedor denominada **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="16846-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="16846-107">Este objeto de contenedor proporciona acceso a una tabla para mostrar que describe el cuadro de diálogo de búsqueda: un cuadro de diálogo se usa para escribir y editar los criterios de búsqueda avanzada.</span><span class="sxs-lookup"><span data-stu-id="16846-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="16846-108">**Para realizar una búsqueda avanzada en un contenedor de la libreta de direcciones**</span><span class="sxs-lookup"><span data-stu-id="16846-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="16846-109">Llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor, especificando **PR_SEARCH** para la etiqueta de propiedad y IID_IMAPIContainer para el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="16846-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="16846-110">Llamar al método **IMAPIProp::OpenProperty** del objeto de la búsqueda, especificando **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) para la etiqueta de propiedad y IID_IMAPITable para el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="16846-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="16846-111">Llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) del objeto de búsqueda para establecer los valores de las propiedades que se utilizará en la búsqueda avanzada.</span><span class="sxs-lookup"><span data-stu-id="16846-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="16846-112">Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del objeto de búsqueda para guardar los criterios de búsqueda avanzada.</span><span class="sxs-lookup"><span data-stu-id="16846-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="16846-113">Esta secuencia de llamadas da como resultado una restricción que están disponibles cuando un cliente llama (método) **es posible GetSearchCriteria** del objeto de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="16846-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

