---
title: Uso de un cuadro de diálogo de búsqueda avanzada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437304"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="9a463-103">Uso de un cuadro de diálogo de búsqueda avanzada</span><span class="sxs-lookup"><span data-stu-id="9a463-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="9a463-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a463-105">Algunos contenedores de libretas de direcciones admiten una capacidad de búsqueda avanzada que permite a los clientes buscar en propiedades distintas de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9a463-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="9a463-106">Los contenedores de libretas de direcciones que admiten búsquedas avanzadas tienen una propiedad de objeto de contenedor denominada **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9a463-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="9a463-107">Este objeto Container proporciona acceso a una tabla de presentación que describe el cuadro de diálogo de búsqueda: un cuadro de diálogo que se usa para escribir y editar los criterios de búsqueda avanzada.</span><span class="sxs-lookup"><span data-stu-id="9a463-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="9a463-108">**Para realizar una búsqueda avanzada en un contenedor de libretas de direcciones**</span><span class="sxs-lookup"><span data-stu-id="9a463-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="9a463-109">Llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor, especificando **PR_SEARCH** para la etiqueta de propiedad y IID_IMAPIContainer para el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="9a463-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="9a463-110">Llame al método **IMAPIProp:: OpenProperty** del objeto Search, especificando **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) para la etiqueta de propiedad y IID_IMAPITable para el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="9a463-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="9a463-111">Llame al método [IMAPIProp:: SetProps](imapiprop-setprops.md) del objeto Search para establecer los valores de las propiedades que se van a usar en la búsqueda avanzada.</span><span class="sxs-lookup"><span data-stu-id="9a463-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="9a463-112">Llame al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del objeto Search para guardar los criterios de búsqueda avanzada.</span><span class="sxs-lookup"><span data-stu-id="9a463-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="9a463-113">Esta secuencia de llamadas da como resultado una restricción que está disponible cuando un cliente llama al método **GetSearchCriteria** del objeto Search.</span><span class="sxs-lookup"><span data-stu-id="9a463-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

