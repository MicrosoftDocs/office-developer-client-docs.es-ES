---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407448"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="7cacd-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="7cacd-103">SizedDtblPage</span></span>

<span data-ttu-id="7cacd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cacd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cacd-105">Crea una estructura con nombre que incluye una estructura [DTBLPAGE](dtblpage.md) para describir un control de página con pestañas, una etiqueta de una longitud especificada y una entrada de archivo de ayuda de una longitud especificada.</span><span class="sxs-lookup"><span data-stu-id="7cacd-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7cacd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7cacd-106">Header file:</span></span>  <br/> |<span data-ttu-id="7cacd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7cacd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7cacd-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="7cacd-108">Related structure:</span></span>  <br/> |<span data-ttu-id="7cacd-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="7cacd-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="7cacd-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="7cacd-110">Parameters</span></span>

<span data-ttu-id="7cacd-111">_n_</span><span class="sxs-lookup"><span data-stu-id="7cacd-111">_n_</span></span>
  
> <span data-ttu-id="7cacd-112">Longitud de la etiqueta de la pestaña de página.</span><span class="sxs-lookup"><span data-stu-id="7cacd-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="7cacd-113">_n1_</span><span class="sxs-lookup"><span data-stu-id="7cacd-113">_n1_</span></span>
  
> <span data-ttu-id="7cacd-114">Longitud de la entrada que aparece en el archivo Mapisvc.inf que identifica el archivo de ayuda que se usará con el control de página con fichas.</span><span class="sxs-lookup"><span data-stu-id="7cacd-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="7cacd-115">_s_</span><span class="sxs-lookup"><span data-stu-id="7cacd-115">_u_</span></span>
  
> <span data-ttu-id="7cacd-116">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="7cacd-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7cacd-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7cacd-117">Remarks</span></span>

<span data-ttu-id="7cacd-118">La **macro SizedDtblPage** permite definir un control de página con pestañas cuando se conoce el número de caracteres de la etiqueta asociada y la entrada del archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="7cacd-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="7cacd-119">La nueva estructura se crea con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="7cacd-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="7cacd-120">Para usar un puntero a la estructura resultante de la macro **SizedDtblPage** como puntero de estructura **DTBLPAGE,** realice la conversión siguiente:</span><span class="sxs-lookup"><span data-stu-id="7cacd-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="7cacd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cacd-121">See also</span></span>

- [<span data-ttu-id="7cacd-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="7cacd-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="7cacd-123">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="7cacd-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

