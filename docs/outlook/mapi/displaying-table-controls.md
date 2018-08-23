---
title: Mostrar controles de la tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7af1e710006986807091c5c36d54da86204a71d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568465"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="15d10-103">Mostrar controles de la tabla</span><span class="sxs-lookup"><span data-stu-id="15d10-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="15d10-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15d10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15d10-105">Existen muchos tipos diferentes de controles, ninguno exclusivas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="15d10-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="15d10-106">Sin embargo, MAPI define sus propias estructuras que se usan en combinación con [BuildDisplayTable](builddisplaytable.md) para describir el único conjunto de datos relacionadas con cada control.</span><span class="sxs-lookup"><span data-stu-id="15d10-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="15d10-107">En la siguiente tabla se enumera las estructuras que describen cada tipo de control.</span><span class="sxs-lookup"><span data-stu-id="15d10-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="15d10-108">**Estructura de control**</span><span class="sxs-lookup"><span data-stu-id="15d10-108">**Control structure**</span></span>|<span data-ttu-id="15d10-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15d10-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15d10-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="15d10-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="15d10-111">Describe un control de botón.</span><span class="sxs-lookup"><span data-stu-id="15d10-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="15d10-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="15d10-113">Describe un control de casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="15d10-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="15d10-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="15d10-115">Describe un control de cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="15d10-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="15d10-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="15d10-117">Describe un control de cuadro de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="15d10-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="15d10-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="15d10-119">Describe un control de edición.</span><span class="sxs-lookup"><span data-stu-id="15d10-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="15d10-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="15d10-121">Describe un control de cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="15d10-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="15d10-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="15d10-123">Describe un control de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="15d10-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="15d10-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="15d10-125">Describe un control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="15d10-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="15d10-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="15d10-127">Describe un control de cuadro de lista desplegable de varios valores.</span><span class="sxs-lookup"><span data-stu-id="15d10-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="15d10-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="15d10-129">Describe un control de cuadro de lista de varios valores.</span><span class="sxs-lookup"><span data-stu-id="15d10-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="15d10-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="15d10-131">Describe un control de páginas con fichas.</span><span class="sxs-lookup"><span data-stu-id="15d10-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="15d10-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="15d10-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="15d10-133">Describe un control de botón de opción.</span><span class="sxs-lookup"><span data-stu-id="15d10-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15d10-134">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="15d10-134">See also</span></span>



[<span data-ttu-id="15d10-135">Implementación de la tabla para mostrar</span><span class="sxs-lookup"><span data-stu-id="15d10-135">Display Table Implementation</span></span>](display-table-implementation.md)

