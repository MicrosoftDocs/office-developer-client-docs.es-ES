---
title: Mostrar controles de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 37f6cd0320894d500416672c3dd0d90ee3324b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422694"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="82257-103">Mostrar controles de tabla</span><span class="sxs-lookup"><span data-stu-id="82257-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="82257-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82257-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82257-105">Hay muchos tipos diferentes de controles, ninguno exclusivo de MAPI.</span><span class="sxs-lookup"><span data-stu-id="82257-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="82257-106">Sin embargo, MAPI define sus propias estructuras que se usan junto con [BuildDisplayTable](builddisplaytable.md) para describir el conjunto único de datos relacionados con cada control.</span><span class="sxs-lookup"><span data-stu-id="82257-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="82257-107">En la tabla siguiente se enumeran las estructuras que describen cada tipo de control.</span><span class="sxs-lookup"><span data-stu-id="82257-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="82257-108">**Estructura de control**</span><span class="sxs-lookup"><span data-stu-id="82257-108">**Control structure**</span></span>|<span data-ttu-id="82257-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82257-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82257-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="82257-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="82257-111">Describe un control de botón.</span><span class="sxs-lookup"><span data-stu-id="82257-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="82257-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="82257-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="82257-113">Describe un control de casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="82257-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="82257-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="82257-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="82257-115">Describe un control de cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="82257-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="82257-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="82257-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="82257-117">Describe un control de cuadro de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="82257-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="82257-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="82257-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="82257-119">Describe un control de edición.</span><span class="sxs-lookup"><span data-stu-id="82257-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="82257-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="82257-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="82257-121">Describe un control de cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="82257-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="82257-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="82257-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="82257-123">Describe un control de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="82257-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="82257-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="82257-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="82257-125">Describe un control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="82257-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="82257-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="82257-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="82257-127">Describe un control de cuadro de lista desplegable de varios valores.</span><span class="sxs-lookup"><span data-stu-id="82257-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="82257-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="82257-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="82257-129">Describe un control de cuadro de lista de varios valores.</span><span class="sxs-lookup"><span data-stu-id="82257-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="82257-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="82257-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="82257-131">Describe un control de página con pestañas.</span><span class="sxs-lookup"><span data-stu-id="82257-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="82257-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="82257-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="82257-133">Describe un control de botón de opción.</span><span class="sxs-lookup"><span data-stu-id="82257-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82257-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="82257-134">See also</span></span>



[<span data-ttu-id="82257-135">Implementación de tabla para mostrar</span><span class="sxs-lookup"><span data-stu-id="82257-135">Display Table Implementation</span></span>](display-table-implementation.md)

