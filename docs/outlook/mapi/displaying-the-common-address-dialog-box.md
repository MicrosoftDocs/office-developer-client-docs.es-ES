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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337096"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="7c487-103">Mostrar el cuadro de diálogo Dirección común</span><span class="sxs-lookup"><span data-stu-id="7c487-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="7c487-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c487-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c487-105">El cuadro de diálogo Dirección común de MAPI se puede usar para varias tareas de direccionamiento, como la creación de una lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="7c487-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="7c487-106">Para mostrar este cuadro de diálogo, llame a **IAddrBook:: Address**.</span><span class="sxs-lookup"><span data-stu-id="7c487-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="7c487-107">Según el número de parámetros que establezca y el modo en que los establezca, puede limitar la visualización a las entradas de un tipo determinado desde un determinado contenedor.</span><span class="sxs-lookup"><span data-stu-id="7c487-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="7c487-108">**Para limitar el cuadro de diálogo de la dirección a mostrar solo las entradas de la libreta personal de direcciones (PAB)**</span><span class="sxs-lookup"><span data-stu-id="7c487-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="7c487-109">Llame a [IAddrBook:: GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la PAB.</span><span class="sxs-lookup"><span data-stu-id="7c487-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="7c487-110">Cree una restricción de propiedad que use RELOP_EQ para el miembro **RELOP** de la estructura [SPropertyRestriction](spropertyrestriction.md) y \*\*\*\* bien el elemento ([PidTagEntryId](pidtagentryid-canonical-property.md)) o **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) como el miembro **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="7c487-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="7c487-111">Si usa el \*\*\*\* valor, pase el identificador de entrada recuperado de **GetPAB**.</span><span class="sxs-lookup"><span data-stu-id="7c487-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="7c487-112">Si usa **PR_AB_PROVIDER_ID**, pase el valor incluido en MSPAB. H archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="7c487-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="7c487-113">**PR_AB_PROVIDER_ID** es el identificador único de la PAB diseñado por MAPI.</span><span class="sxs-lookup"><span data-stu-id="7c487-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="7c487-114">Llamar a [IAddrBook:: Address](iaddrbook-address.md) con el parámetro _lpHierRestriction_ que apunte a la restricción de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7c487-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

