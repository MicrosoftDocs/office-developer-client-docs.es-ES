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
ms.openlocfilehash: 9295c37a46d3566089f708aaaa0b9fc3b5f30db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816740"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="2bfe8-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="2bfe8-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="2bfe8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2bfe8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2bfe8-105">Describe un control de cuadro de grupo que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="2bfe8-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2bfe8-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2bfe8-106">Header file:</span></span>  <br/> |<span data-ttu-id="2bfe8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2bfe8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2bfe8-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="2bfe8-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="2bfe8-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="2bfe8-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="2bfe8-110">Members</span><span class="sxs-lookup"><span data-stu-id="2bfe8-110">Members</span></span>

 <span data-ttu-id="2bfe8-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="2bfe8-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="2bfe8-112">Posición en la memoria de la cadena de caracteres que acompaña al cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="2bfe8-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="2bfe8-113">Si aparece, la etiqueta aparece en la parte superior, izquierda del cuadro.</span><span class="sxs-lookup"><span data-stu-id="2bfe8-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="2bfe8-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="2bfe8-114">**ulFlags**</span></span>
  
> <span data-ttu-id="2bfe8-115">Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="2bfe8-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="2bfe8-116">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="2bfe8-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="2bfe8-117">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="2bfe8-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2bfe8-118">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="2bfe8-118">The label is in Unicode format.</span></span> <span data-ttu-id="2bfe8-119">Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="2bfe8-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2bfe8-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2bfe8-120">Remarks</span></span>

<span data-ttu-id="2bfe8-121">Una estructura **DTBLGROUPBOX** describe un control de cuadro de grupo que se usa para asociar visualmente otros controles en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2bfe8-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="2bfe8-122">La técnica con resaltado de coincidencias implica que rodea los otros controles por un cuadro.</span><span class="sxs-lookup"><span data-stu-id="2bfe8-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="2bfe8-123">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2bfe8-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="2bfe8-124">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="2bfe8-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2bfe8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bfe8-125">See also</span></span>



[<span data-ttu-id="2bfe8-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="2bfe8-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="2bfe8-127">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="2bfe8-127">MAPI Structures</span></span>](mapi-structures.md)

