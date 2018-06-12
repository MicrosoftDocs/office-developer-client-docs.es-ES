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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820691"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="13989-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="13989-103">SizedDtblLabel</span></span>

<span data-ttu-id="13989-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13989-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13989-105">Crea una estructura con nombre que incluye una estructura [DTBLLABEL](dtbllabel.md) para describir un control de etiqueta y la etiqueta asociada de una longitud especificada.</span><span class="sxs-lookup"><span data-stu-id="13989-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13989-106">Especificado en el archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="13989-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="13989-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13989-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="13989-108">Estructura relacionado</span><span class="sxs-lookup"><span data-stu-id="13989-108">Related structure</span></span>  <br/> |<span data-ttu-id="13989-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="13989-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="13989-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13989-110">Parameters</span></span>

<span data-ttu-id="13989-111">_n_</span><span class="sxs-lookup"><span data-stu-id="13989-111">_n_</span></span>
  
> <span data-ttu-id="13989-112">Longitud de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="13989-112">Length of the label.</span></span> <span data-ttu-id="13989-113">Esto incluye el carácter nulo final.</span><span class="sxs-lookup"><span data-stu-id="13989-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="13989-114">_u_</span><span class="sxs-lookup"><span data-stu-id="13989-114">_u_</span></span>
  
> <span data-ttu-id="13989-115">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="13989-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13989-116">Notas</span><span class="sxs-lookup"><span data-stu-id="13989-116">Remarks</span></span>

<span data-ttu-id="13989-117">La macro **SizedDtblLabel** le permite definir una etiqueta de tabla para mostrar cuando se conoce el número de caracteres en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="13989-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="13989-118">Se crea la nueva estructura con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="13989-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="13989-119">Para utilizar un puntero a la estructura resultante de la macro **SizedDtblLabel** como un puntero de estructura **DTBLLABEL** , realizar la conversión a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="13989-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="13989-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="13989-120">See also</span></span>

- [<span data-ttu-id="13989-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="13989-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="13989-122">Macros relacionadas con las estructuras</span><span class="sxs-lookup"><span data-stu-id="13989-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

