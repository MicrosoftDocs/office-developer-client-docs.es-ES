---
title: Implementación de búsquedas avanzadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407392"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="d26b0-103">Implementación de búsquedas avanzadas</span><span class="sxs-lookup"><span data-stu-id="d26b0-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="d26b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d26b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d26b0-105">Algunos contenedores de libretas de direcciones admiten una capacidad de búsqueda avanzada que permite a los clientes buscar en propiedades distintas de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d26b0-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="d26b0-106">Para admitir búsquedas avanzadas, el proveedor debe implementar un contenedor especial al que se pueda tener acceso a través de la propiedad **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de los otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="d26b0-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="d26b0-107">**PR_SEARCH** contiene un objeto Container que proporciona acceso a una tabla de presentación que describe el cuadro de diálogo usado para escribir y editar los criterios de búsqueda avanzada.</span><span class="sxs-lookup"><span data-stu-id="d26b0-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="d26b0-108">**Para admitir la búsqueda avanzada**</span><span class="sxs-lookup"><span data-stu-id="d26b0-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="d26b0-109">Defina una propiedad para cada uno de los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d26b0-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="d26b0-110">En la sección de código del método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor que controla la propiedad **PR_SEARCH** :</span><span class="sxs-lookup"><span data-stu-id="d26b0-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="d26b0-111">Compruebe que el cliente está solicitando la interfaz **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="d26b0-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="d26b0-112">Si se solicita una interfaz inapropiada, se produce un error y se devuelve MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="d26b0-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="d26b0-113">Cree un nuevo objeto Search que admita la interfaz **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="d26b0-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="d26b0-114">En este momento, se realizará una llamada al método **IMAPIProp:: OpenProperty** del contenedor de búsqueda para recuperar su propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d26b0-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="d26b0-115">El proveedor debe proporcionar una tabla de presentación, normalmente a través de una llamada a [BuildDisplayTable](builddisplaytable.md), que describe el cuadro de diálogo búsqueda avanzada del contenedor.</span><span class="sxs-lookup"><span data-stu-id="d26b0-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="d26b0-116">MAPI muestra el cuadro de diálogo de búsqueda, lo que permite al usuario especificar los criterios adecuados.</span><span class="sxs-lookup"><span data-stu-id="d26b0-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="d26b0-117">Cuando el usuario ha terminado, MAPI llama al método [IMAPIProp:: SetProps](imapiprop-setprops.md) del contenedor para almacenar los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d26b0-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="d26b0-118">Se realizará una llamada para solicitar la tabla de contenido del contenedor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d26b0-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="d26b0-119">ReLlene la tabla Contents con todas las entradas del contenedor que coinciden con los criterios.</span><span class="sxs-lookup"><span data-stu-id="d26b0-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

