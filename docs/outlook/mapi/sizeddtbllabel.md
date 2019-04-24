---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282708"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="74862-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="74862-103">SizedDtblLabel</span></span>

<span data-ttu-id="74862-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74862-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74862-105">Crea una estructura con nombre que incluye una estructura [DTBLLABEL](dtbllabel.md) para describir un control de etiqueta y la etiqueta asociada de una longitud determinada.</span><span class="sxs-lookup"><span data-stu-id="74862-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74862-106">Especificado en el archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="74862-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="74862-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="74862-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="74862-108">Estructura relacionada</span><span class="sxs-lookup"><span data-stu-id="74862-108">Related structure</span></span>  <br/> |<span data-ttu-id="74862-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="74862-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="74862-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="74862-110">Parameters</span></span>

<span data-ttu-id="74862-111">_n_</span><span class="sxs-lookup"><span data-stu-id="74862-111">_n_</span></span>
  
> <span data-ttu-id="74862-112">Longitud de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="74862-112">Length of the label.</span></span> <span data-ttu-id="74862-113">Esto incluye el carácter NULL final.</span><span class="sxs-lookup"><span data-stu-id="74862-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="74862-114">_u_</span><span class="sxs-lookup"><span data-stu-id="74862-114">_u_</span></span>
  
> <span data-ttu-id="74862-115">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="74862-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74862-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74862-116">Remarks</span></span>

<span data-ttu-id="74862-117">La macro **SizedDtblLabel** permite definir una etiqueta de tabla de visualización cuando se conoce el número de caracteres de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="74862-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="74862-118">La nueva estructura se crea con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="74862-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="74862-119">Para usar un puntero a la estructura resultante desde la macro **SizedDtblLabel** como un puntero de estructura **DTBLLABEL** , realice la siguiente conversión:</span><span class="sxs-lookup"><span data-stu-id="74862-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="74862-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="74862-120">See also</span></span>

- [<span data-ttu-id="74862-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="74862-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="74862-122">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="74862-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

