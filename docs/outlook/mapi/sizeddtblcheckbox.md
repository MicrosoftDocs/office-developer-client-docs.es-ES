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
ms.openlocfilehash: 9a30554253bc11c8905273079429e4b41c20583a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820669"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="52865-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="52865-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="52865-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52865-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52865-105">Crea una estructura con nombre que incluye una estructura [DTBLCHECKBOX](dtblcheckbox.md) para describir un control de casilla de verificación y una etiqueta de un período especificado.</span><span class="sxs-lookup"><span data-stu-id="52865-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52865-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="52865-106">Header file:</span></span>  <br/> |<span data-ttu-id="52865-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52865-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="52865-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="52865-108">Related structure:</span></span>  <br/> |<span data-ttu-id="52865-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="52865-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="52865-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52865-110">Parameters</span></span>

<span data-ttu-id="52865-111">_n_</span><span class="sxs-lookup"><span data-stu-id="52865-111">_n_</span></span>
  
> <span data-ttu-id="52865-112">Longitud de la etiqueta que se deben incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="52865-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="52865-113">_s_</span><span class="sxs-lookup"><span data-stu-id="52865-113">_u_</span></span>
  
> <span data-ttu-id="52865-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="52865-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="52865-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52865-115">Remarks</span></span>

<span data-ttu-id="52865-116">La macro **SizedDtblCheckBox** le permite definir una casilla de verificación cuando se conoce el número de caracteres de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="52865-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="52865-117">Se crea la nueva estructura con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="52865-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="52865-118">Para utilizar un puntero a la estructura resultante de la macro **SizedDtblCheckBox** como un puntero de estructura **DTBLCHECKBOX** , realizar la conversión a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="52865-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="52865-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="52865-119">See also</span></span>

- [<span data-ttu-id="52865-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="52865-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="52865-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="52865-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

