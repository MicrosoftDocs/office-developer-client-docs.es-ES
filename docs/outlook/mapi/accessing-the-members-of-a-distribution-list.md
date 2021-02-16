---
title: Acceso a los miembros de una lista de distribución
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2944a53d27bc916ccafcfa649d79e3c00afaf622
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412390"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="69b7f-103">Acceso a los miembros de una lista de distribución</span><span class="sxs-lookup"><span data-stu-id="69b7f-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="69b7f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69b7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="69b7f-105">**Para obtener los miembros de una lista de distribución**</span><span class="sxs-lookup"><span data-stu-id="69b7f-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="69b7f-106">Cree una matriz de etiquetas de propiedad de tamaño con las propiedades de los miembros que desea recuperar, como **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="69b7f-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="69b7f-107">Llame [a IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="69b7f-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="69b7f-108">Llama al método **IABContainer::GetContentsTable** de la lista de distribución para obtener acceso a su tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="69b7f-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="69b7f-109">Llame [a HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas de la tabla que representan a los miembros de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="69b7f-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

