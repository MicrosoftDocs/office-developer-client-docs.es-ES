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
ms.openlocfilehash: a7d62d29638ae234667eb33a8103fb3a716afc32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421917"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="f042f-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="f042f-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="f042f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f042f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f042f-105">Crea una estructura con nombre que incluye una [estructura DTBLBUTTON](dtblbutton.md) para describir un botón y una etiqueta de una longitud especificada.</span><span class="sxs-lookup"><span data-stu-id="f042f-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f042f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f042f-106">Header file:</span></span>  <br/> |<span data-ttu-id="f042f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f042f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f042f-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="f042f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="f042f-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="f042f-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="f042f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f042f-110">Parameters</span></span>

 <span data-ttu-id="f042f-111">_n_</span><span class="sxs-lookup"><span data-stu-id="f042f-111">_n_</span></span>
  
> <span data-ttu-id="f042f-112">Longitud de la etiqueta que se incluirá en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="f042f-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="f042f-113">_s_</span><span class="sxs-lookup"><span data-stu-id="f042f-113">_u_</span></span>
  
> <span data-ttu-id="f042f-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="f042f-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f042f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f042f-115">Remarks</span></span>

<span data-ttu-id="f042f-116">La nueva estructura se crea con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="f042f-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="f042f-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f042f-117">See also</span></span>



[<span data-ttu-id="f042f-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="f042f-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="f042f-119">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="f042f-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

