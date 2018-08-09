---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820667"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="45884-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="45884-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="45884-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45884-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45884-105">Crea una estructura con nombre que incluye una estructura [DTBLBUTTON](dtblbutton.md) para describir un botón y una etiqueta de un período especificado.</span><span class="sxs-lookup"><span data-stu-id="45884-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45884-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="45884-106">Header file:</span></span>  <br/> |<span data-ttu-id="45884-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45884-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="45884-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="45884-108">Related structure:</span></span>  <br/> |<span data-ttu-id="45884-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="45884-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="45884-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45884-110">Parameters</span></span>

 <span data-ttu-id="45884-111">_n_</span><span class="sxs-lookup"><span data-stu-id="45884-111">_n_</span></span>
  
> <span data-ttu-id="45884-112">Longitud de la etiqueta que se deben incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="45884-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="45884-113">_s_</span><span class="sxs-lookup"><span data-stu-id="45884-113">_u_</span></span>
  
> <span data-ttu-id="45884-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="45884-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45884-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="45884-115">Remarks</span></span>

<span data-ttu-id="45884-116">Se crea la nueva estructura con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="45884-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="45884-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="45884-117">See also</span></span>



[<span data-ttu-id="45884-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="45884-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="45884-119">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="45884-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

