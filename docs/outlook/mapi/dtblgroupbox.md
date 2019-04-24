---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338664"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="e1eca-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="e1eca-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="e1eca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1eca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1eca-105">Describe un control de cuadro de grupo que se utilizará en un cuadro de diálogo generado a partir de una tabla de presentación.</span><span class="sxs-lookup"><span data-stu-id="e1eca-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1eca-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e1eca-106">Header file:</span></span>  <br/> |<span data-ttu-id="e1eca-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e1eca-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e1eca-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="e1eca-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="e1eca-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="e1eca-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="e1eca-110">Members</span><span class="sxs-lookup"><span data-stu-id="e1eca-110">Members</span></span>

 <span data-ttu-id="e1eca-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="e1eca-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="e1eca-112">Posición en la memoria de la cadena de caracteres que acompaña al cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="e1eca-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="e1eca-113">Si se muestra, la etiqueta aparece en la parte superior izquierda del cuadro.</span><span class="sxs-lookup"><span data-stu-id="e1eca-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="e1eca-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e1eca-114">**ulFlags**</span></span>
  
> <span data-ttu-id="e1eca-115">Máscara de la máscara usada para designar el formato de la etiqueta a la que señala el miembro **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="e1eca-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="e1eca-116">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="e1eca-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="e1eca-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e1eca-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e1eca-118">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e1eca-118">The label is in Unicode format.</span></span> <span data-ttu-id="e1eca-119">Si no se establece la marca MAPI_UNICODE, la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e1eca-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1eca-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1eca-120">Remarks</span></span>

<span data-ttu-id="e1eca-121">Una estructura **DTBLGROUPBOX** describe un control de cuadro de grupo que se usa para asociar visualmente otros controles en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e1eca-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="e1eca-122">La técnica de resaltado implica rodear los demás controles por un cuadro.</span><span class="sxs-lookup"><span data-stu-id="e1eca-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="e1eca-123">Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e1eca-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e1eca-124">Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e1eca-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1eca-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1eca-125">See also</span></span>



[<span data-ttu-id="e1eca-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e1eca-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="e1eca-127">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="e1eca-127">MAPI Structures</span></span>](mapi-structures.md)

