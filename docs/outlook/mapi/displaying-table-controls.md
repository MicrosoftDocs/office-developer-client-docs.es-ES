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
ms.openlocfilehash: 11b3279582c4cfb0d2c2249c6f4eddd7f0260b49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816702"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="3500b-103">Mostrar controles de la tabla</span><span class="sxs-lookup"><span data-stu-id="3500b-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="3500b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3500b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3500b-105">Existen muchos tipos diferentes de controles, ninguno exclusivas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3500b-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="3500b-106">Sin embargo, MAPI define sus propias estructuras que se usan en combinación con [BuildDisplayTable](builddisplaytable.md) para describir el único conjunto de datos relacionadas con cada control.</span><span class="sxs-lookup"><span data-stu-id="3500b-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="3500b-107">En la siguiente tabla se enumera las estructuras que describen cada tipo de control.</span><span class="sxs-lookup"><span data-stu-id="3500b-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="3500b-108">**Estructura de control**</span><span class="sxs-lookup"><span data-stu-id="3500b-108">**Control structure**</span></span>|<span data-ttu-id="3500b-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3500b-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3500b-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="3500b-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="3500b-111">Describe un control de botón.</span><span class="sxs-lookup"><span data-stu-id="3500b-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="3500b-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="3500b-113">Describe un control de casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="3500b-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="3500b-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="3500b-115">Describe un control de cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="3500b-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="3500b-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="3500b-117">Describe un control de cuadro de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="3500b-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="3500b-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="3500b-119">Describe un control de edición.</span><span class="sxs-lookup"><span data-stu-id="3500b-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="3500b-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="3500b-121">Describe un control de cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="3500b-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="3500b-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="3500b-123">Describe un control de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="3500b-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="3500b-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="3500b-125">Describe un control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="3500b-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="3500b-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="3500b-127">Describe un control de cuadro de lista desplegable de varios valores.</span><span class="sxs-lookup"><span data-stu-id="3500b-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="3500b-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="3500b-129">Describe un control de cuadro de lista de varios valores.</span><span class="sxs-lookup"><span data-stu-id="3500b-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="3500b-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="3500b-131">Describe un control de páginas con fichas.</span><span class="sxs-lookup"><span data-stu-id="3500b-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="3500b-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="3500b-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="3500b-133">Describe un control de botón de opción.</span><span class="sxs-lookup"><span data-stu-id="3500b-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3500b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3500b-134">See also</span></span>



[<span data-ttu-id="3500b-135">Implementación de la tabla para mostrar</span><span class="sxs-lookup"><span data-stu-id="3500b-135">Display Table Implementation</span></span>](display-table-implementation.md)

