---
title: Implementar la búsqueda avanzada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4430b52b470b89bd7d81922b98b121b3a455768f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817681"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="a6e22-103">Implementar la búsqueda avanzada</span><span class="sxs-lookup"><span data-stu-id="a6e22-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="a6e22-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6e22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6e22-105">Algunos contenedores de la libreta de direcciones compatible con una capacidad de búsqueda avanzada que permite a los clientes buscar en las propiedades que no sean **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a6e22-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="a6e22-106">Para admitir búsquedas avanzadas, su proveedor debe implementar un contenedor especial que es accesible a través de la propiedad **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de los otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="a6e22-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="a6e22-107">**PR_SEARCH** contiene un objeto de contenedor que proporciona acceso a una tabla para mostrar que describe el cuadro de diálogo se usa para escribir y editar los criterios de búsqueda avanzada.</span><span class="sxs-lookup"><span data-stu-id="a6e22-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="a6e22-108">**Para admitir la búsqueda avanzada**</span><span class="sxs-lookup"><span data-stu-id="a6e22-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="a6e22-109">Definir una propiedad para cada uno de los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a6e22-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="a6e22-110">En la sección de código en método del contenedor de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) que controla la propiedad **PR_SEARCH** :</span><span class="sxs-lookup"><span data-stu-id="a6e22-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="a6e22-111">Compruebe que el cliente está solicitando la interfaz **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="a6e22-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="a6e22-112">Si se solicita una interfaz inapropiada, se producirá un error y devolver MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="a6e22-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="a6e22-113">Crear un nuevo objeto de búsqueda que admite la interfaz **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="a6e22-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="a6e22-114">En este momento, se realiza una llamada al método de **IMAPIProp::OpenProperty** del contenedor de la búsqueda para recuperar su propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a6e22-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="a6e22-115">El proveedor debe proporcionar una tabla para mostrar, normalmente a través de una llamada a [BuildDisplayTable](builddisplaytable.md), que se describe el cuadro de diálogo de búsqueda avanzada del contenedor.</span><span class="sxs-lookup"><span data-stu-id="a6e22-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="a6e22-116">MAPI muestra el cuadro de diálogo Buscar, lo que permite al usuario que escriba los criterios adecuados.</span><span class="sxs-lookup"><span data-stu-id="a6e22-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="a6e22-117">Cuando el usuario ha terminado, MAPI llama al método [IMAPIProp::SetProps](imapiprop-setprops.md) del contenedor para almacenar los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a6e22-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="a6e22-118">Se realizará una llamada para solicitar la tabla de contenido del contenedor de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a6e22-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="a6e22-119">Rellenar la tabla de contenido con todas las entradas en el contenedor que coinciden con los criterios.</span><span class="sxs-lookup"><span data-stu-id="a6e22-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

