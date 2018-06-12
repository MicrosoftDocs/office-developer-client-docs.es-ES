---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 4ea77023bdc9442325f4af46d23c107e7172ceaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820674"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="d8ce0-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="d8ce0-103">SizedDtblEdit</span></span>

<span data-ttu-id="d8ce0-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8ce0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8ce0-105">Crea una estructura con nombre que incluye una estructura [DTBLEDIT](dtbledit.md) para describir un control de edición y el número máximo de caracteres que se puede escribir en el control.</span><span class="sxs-lookup"><span data-stu-id="d8ce0-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8ce0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d8ce0-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8ce0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8ce0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d8ce0-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="d8ce0-108">Related structure:</span></span>  <br/> |<span data-ttu-id="d8ce0-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="d8ce0-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="d8ce0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8ce0-110">Parameters</span></span>

<span data-ttu-id="d8ce0-111">_n_</span><span class="sxs-lookup"><span data-stu-id="d8ce0-111">_n_</span></span>
  
> <span data-ttu-id="d8ce0-112">Número máximo de caracteres que se puede escribir en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="d8ce0-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="d8ce0-113">_u_</span><span class="sxs-lookup"><span data-stu-id="d8ce0-113">_u_</span></span>
  
> <span data-ttu-id="d8ce0-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="d8ce0-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8ce0-115">Notas</span><span class="sxs-lookup"><span data-stu-id="d8ce0-115">Remarks</span></span>

<span data-ttu-id="d8ce0-116">La macro **SizedDtblEdit** le permite definir un control de edición cuando se conoce el número de caracteres habilitados.</span><span class="sxs-lookup"><span data-stu-id="d8ce0-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="d8ce0-117">Se crea la nueva estructura con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="d8ce0-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="d8ce0-118">Para utilizar un puntero a la estructura resultante de la macro **SizedDtblEdit** como un puntero de estructura **DTBLEDIT** , realizar la conversión a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="d8ce0-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="d8ce0-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="d8ce0-119">See also</span></span>

- [<span data-ttu-id="d8ce0-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="d8ce0-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="d8ce0-121">Macros relacionadas con las estructuras</span><span class="sxs-lookup"><span data-stu-id="d8ce0-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

