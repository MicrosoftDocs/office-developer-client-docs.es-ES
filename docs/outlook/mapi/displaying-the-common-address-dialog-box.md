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
ms.openlocfilehash: a7b603504956be9ec3066e5ff5e1d5db7d59852a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816715"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="3cc04-103">Mostrar el cuadro de diálogo Dirección común</span><span class="sxs-lookup"><span data-stu-id="3cc04-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="3cc04-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3cc04-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3cc04-105">El cuadro de diálogo dirección común de MAPI puede usarse para una variedad de hacer frente a tareas como la construcción de una lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="3cc04-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="3cc04-106">Para mostrar este cuadro de diálogo, llame a **IAddrBook::Address**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="3cc04-107">Dependiendo de cuál de los muchos parámetros que defina y cómo establecer, puede limitar la presentación a las entradas de un tipo determinado de un contenedor determinado.</span><span class="sxs-lookup"><span data-stu-id="3cc04-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="3cc04-108">**Para limitar el cuadro de diálogo dirección para mostrar sólo las entradas de (PAB) de la libreta de direcciones personales**</span><span class="sxs-lookup"><span data-stu-id="3cc04-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="3cc04-109">Llame a [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la Libreta personal de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3cc04-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="3cc04-110">Crear una restricción de propiedad que usa RELOP_EQ para el miembro **relop** de la estructura de [SPropertyRestriction](spropertyrestriction.md) y **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) o **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) como el miembro de **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="3cc04-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="3cc04-111">Si utiliza la **entrada del objeto**, pase el identificador de entrada recuperado de **GetPAB**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="3cc04-112">Si usa **PR_AB_PROVIDER_ID**, pase el valor incluido en el MSPAB. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="3cc04-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="3cc04-113">**PR_AB_PROVIDER_ID** es el identificador único para el archivo PAB diseñado por MAPI.</span><span class="sxs-lookup"><span data-stu-id="3cc04-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="3cc04-114">Llame al método [IAddrBook::Address](iaddrbook-address.md) con el parámetro _lpHierRestriction_ que señala a la restricción de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3cc04-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

