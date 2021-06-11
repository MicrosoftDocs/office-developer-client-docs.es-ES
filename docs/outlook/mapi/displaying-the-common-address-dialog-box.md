---
title: Mostrar el cuadro de diálogo Dirección común
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436907"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="cac45-103">Mostrar el cuadro de diálogo Dirección común</span><span class="sxs-lookup"><span data-stu-id="cac45-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="cac45-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cac45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cac45-105">El cuadro de diálogo dirección común MAPI se puede usar para una variedad de tareas de direccionamiento, como la construcción de una lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="cac45-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="cac45-106">Para mostrar este cuadro de diálogo, llame a **IAddrBook::Address**.</span><span class="sxs-lookup"><span data-stu-id="cac45-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="cac45-107">Según cuál de los muchos parámetros que establezca y cómo los establezca, puede limitar la presentación a las entradas de un tipo determinado de un contenedor determinado.</span><span class="sxs-lookup"><span data-stu-id="cac45-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="cac45-108">**Para limitar el cuadro de diálogo de direcciones a mostrar solo entradas de libreta de direcciones personal (PAB)**</span><span class="sxs-lookup"><span data-stu-id="cac45-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="cac45-109">Llama [a IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada del PAB.</span><span class="sxs-lookup"><span data-stu-id="cac45-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="cac45-110">Cree una restricción de propiedad que use RELOP_EQ para el miembro **relop** de la estructura [SPropertyRestriction](spropertyrestriction.md) y **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) o **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) como **miembro de ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="cac45-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="cac45-111">Si usa **PR_ENTRYID**, pase el identificador de entrada recuperado de **GetPAB**.</span><span class="sxs-lookup"><span data-stu-id="cac45-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="cac45-112">Si usa **PR_AB_PROVIDER_ID**, pase el valor incluido en la MSPAB. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="cac45-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="cac45-113">**PR_AB_PROVIDER_ID** es el identificador único de la PAB diseñada por MAPI.</span><span class="sxs-lookup"><span data-stu-id="cac45-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="cac45-114">Llama [a IAddrBook::Address con](iaddrbook-address.md) el parámetro  _lpHierRestriction_ que apunta a la restricción de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cac45-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

