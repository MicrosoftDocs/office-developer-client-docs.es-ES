---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420811"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="9f4f6-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="9f4f6-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="9f4f6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f4f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f4f6-105">Crea una estructura con nombre que incluye una [estructura DTBLCHECKBOX](dtblcheckbox.md) para describir un control de casilla de verificación y una etiqueta de una longitud especificada.</span><span class="sxs-lookup"><span data-stu-id="9f4f6-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f4f6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9f4f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f4f6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f4f6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9f4f6-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="9f4f6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="9f4f6-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="9f4f6-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="9f4f6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f4f6-110">Parameters</span></span>

<span data-ttu-id="9f4f6-111">_n_</span><span class="sxs-lookup"><span data-stu-id="9f4f6-111">_n_</span></span>
  
> <span data-ttu-id="9f4f6-112">Longitud de la etiqueta que se incluirá en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="9f4f6-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="9f4f6-113">_s_</span><span class="sxs-lookup"><span data-stu-id="9f4f6-113">_u_</span></span>
  
> <span data-ttu-id="9f4f6-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="9f4f6-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f4f6-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f4f6-115">Remarks</span></span>

<span data-ttu-id="9f4f6-116">La macro **SizedDtblCheckBox** permite definir una casilla cuando se conoce el número de caracteres de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="9f4f6-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="9f4f6-117">La nueva estructura se crea con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="9f4f6-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="9f4f6-118">Para usar un puntero a la estructura resultante de la macro **SizedDtblCheckBox** como puntero de estructura **DTBLCHECKBOX,** realice la conversión siguiente:</span><span class="sxs-lookup"><span data-stu-id="9f4f6-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="9f4f6-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9f4f6-119">See also</span></span>

- [<span data-ttu-id="9f4f6-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="9f4f6-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="9f4f6-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="9f4f6-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

