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
# <a name="displaying-table-controls"></a><span data-ttu-id="a30ff-103">Mostrar controles de tabla</span><span class="sxs-lookup"><span data-stu-id="a30ff-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="a30ff-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a30ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a30ff-105">Hay muchos tipos diferentes de controles, ninguno único de MAPI.</span><span class="sxs-lookup"><span data-stu-id="a30ff-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="a30ff-106">Sin embargo, MAPI define sus propias estructuras que se usan junto con [BuildDisplayTable](builddisplaytable.md) para describir el conjunto único de datos implicados en cada control.</span><span class="sxs-lookup"><span data-stu-id="a30ff-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="a30ff-107">En la siguiente tabla se enumeran las estructuras que describen cada tipo de control.</span><span class="sxs-lookup"><span data-stu-id="a30ff-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="a30ff-108">**Estructura de control**</span><span class="sxs-lookup"><span data-stu-id="a30ff-108">**Control structure**</span></span>|<span data-ttu-id="a30ff-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a30ff-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a30ff-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="a30ff-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="a30ff-111">Describe un control de botón.</span><span class="sxs-lookup"><span data-stu-id="a30ff-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="a30ff-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="a30ff-113">Describe un control de casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="a30ff-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="a30ff-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="a30ff-115">Describe un control de cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="a30ff-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="a30ff-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="a30ff-117">Describe un control de cuadro de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="a30ff-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="a30ff-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="a30ff-119">Describe un control de edición.</span><span class="sxs-lookup"><span data-stu-id="a30ff-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="a30ff-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="a30ff-121">Describe un control de cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="a30ff-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="a30ff-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="a30ff-123">Describe un control de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a30ff-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="a30ff-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="a30ff-125">Describe un control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="a30ff-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="a30ff-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="a30ff-127">Describe un control de cuadro de lista desplegable de varios valores.</span><span class="sxs-lookup"><span data-stu-id="a30ff-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="a30ff-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="a30ff-129">Describe un control de cuadro de lista con varios valores.</span><span class="sxs-lookup"><span data-stu-id="a30ff-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="a30ff-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="a30ff-131">Describe un control de página con fichas.</span><span class="sxs-lookup"><span data-stu-id="a30ff-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="a30ff-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="a30ff-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="a30ff-133">Describe un control de botón de opción.</span><span class="sxs-lookup"><span data-stu-id="a30ff-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a30ff-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="a30ff-134">See also</span></span>



[<span data-ttu-id="a30ff-135">Implementación de la tabla de visualización</span><span class="sxs-lookup"><span data-stu-id="a30ff-135">Display Table Implementation</span></span>](display-table-implementation.md)

