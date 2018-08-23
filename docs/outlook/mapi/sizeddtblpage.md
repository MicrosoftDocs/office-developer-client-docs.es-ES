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
ms.openlocfilehash: ae3f84c6b219c7becb88737f0d6c9fcb9722ea34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584971"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="019d6-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="019d6-103">SizedDtblPage</span></span>

<span data-ttu-id="019d6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="019d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="019d6-105">Crea una estructura con nombre que incluye una estructura [DTBLPAGE](dtblpage.md) para describir un control de páginas con fichas, una etiqueta de un período especificado y una entrada de archivo de Ayuda de una longitud especificada.</span><span class="sxs-lookup"><span data-stu-id="019d6-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="019d6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="019d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="019d6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="019d6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="019d6-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="019d6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="019d6-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="019d6-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="019d6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="019d6-110">Parameters</span></span>

<span data-ttu-id="019d6-111">_n_</span><span class="sxs-lookup"><span data-stu-id="019d6-111">_n_</span></span>
  
> <span data-ttu-id="019d6-112">Longitud de la etiqueta de la ficha página.</span><span class="sxs-lookup"><span data-stu-id="019d6-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="019d6-113">_N1_</span><span class="sxs-lookup"><span data-stu-id="019d6-113">_n1_</span></span>
  
> <span data-ttu-id="019d6-114">Longitud de la entrada que aparece en el archivo Mapisvc.inf que identifica el archivo de ayuda que se utilizará junto con el control de la página con fichas.</span><span class="sxs-lookup"><span data-stu-id="019d6-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="019d6-115">_s_</span><span class="sxs-lookup"><span data-stu-id="019d6-115">_u_</span></span>
  
> <span data-ttu-id="019d6-116">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="019d6-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="019d6-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="019d6-117">Remarks</span></span>

<span data-ttu-id="019d6-118">La macro **SizedDtblPage** le permite definir un control de páginas con fichas cuando se conoce el número de caracteres en la etiqueta asociada y la entrada del archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="019d6-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="019d6-119">Se crea la nueva estructura con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="019d6-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="019d6-120">Para utilizar un puntero a la estructura resultante de la macro **SizedDtblPage** como un puntero de estructura **DTBLPAGE** , realizar la conversión a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="019d6-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="019d6-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="019d6-121">See also</span></span>

- [<span data-ttu-id="019d6-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="019d6-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="019d6-123">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="019d6-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

