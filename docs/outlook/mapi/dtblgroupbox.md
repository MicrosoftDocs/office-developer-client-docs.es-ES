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
ms.openlocfilehash: ef38893c9ad44556cc9220809b5e407f86fd2642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576319"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="1d9a9-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="1d9a9-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="1d9a9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d9a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d9a9-105">Describe un control de cuadro de grupo que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="1d9a9-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1d9a9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1d9a9-106">Header file:</span></span>  <br/> |<span data-ttu-id="1d9a9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d9a9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1d9a9-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="1d9a9-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="1d9a9-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="1d9a9-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="1d9a9-110">Members</span><span class="sxs-lookup"><span data-stu-id="1d9a9-110">Members</span></span>

 <span data-ttu-id="1d9a9-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="1d9a9-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="1d9a9-112">Posición en la memoria de la cadena de caracteres que acompaña al cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="1d9a9-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="1d9a9-113">Si aparece, la etiqueta aparece en la parte superior, izquierda del cuadro.</span><span class="sxs-lookup"><span data-stu-id="1d9a9-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="1d9a9-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="1d9a9-114">**ulFlags**</span></span>
  
> <span data-ttu-id="1d9a9-115">Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="1d9a9-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="1d9a9-116">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="1d9a9-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="1d9a9-117">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="1d9a9-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1d9a9-118">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1d9a9-118">The label is in Unicode format.</span></span> <span data-ttu-id="1d9a9-119">Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1d9a9-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d9a9-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d9a9-120">Remarks</span></span>

<span data-ttu-id="1d9a9-121">Una estructura **DTBLGROUPBOX** describe un control de cuadro de grupo que se usa para asociar visualmente otros controles en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1d9a9-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="1d9a9-122">La técnica con resaltado de coincidencias implica que rodea los otros controles por un cuadro.</span><span class="sxs-lookup"><span data-stu-id="1d9a9-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="1d9a9-123">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a9-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="1d9a9-124">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a9-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1d9a9-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1d9a9-125">See also</span></span>



[<span data-ttu-id="1d9a9-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="1d9a9-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="1d9a9-127">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="1d9a9-127">MAPI Structures</span></span>](mapi-structures.md)

