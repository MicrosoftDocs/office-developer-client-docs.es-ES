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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e50589b52f3e99bf2569a55bb7d3ca4f8247fd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591663"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="27593-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="27593-103">SizedDtblEdit</span></span>

<span data-ttu-id="27593-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27593-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27593-105">Crea una estructura con nombre que incluye una estructura [DTBLEDIT](dtbledit.md) para describir un control de edición y el número máximo de caracteres que se puede escribir en el control.</span><span class="sxs-lookup"><span data-stu-id="27593-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27593-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="27593-106">Header file:</span></span>  <br/> |<span data-ttu-id="27593-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27593-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="27593-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="27593-108">Related structure:</span></span>  <br/> |<span data-ttu-id="27593-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="27593-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="27593-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27593-110">Parameters</span></span>

<span data-ttu-id="27593-111">_n_</span><span class="sxs-lookup"><span data-stu-id="27593-111">_n_</span></span>
  
> <span data-ttu-id="27593-112">Número máximo de caracteres que se puede escribir en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="27593-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="27593-113">_s_</span><span class="sxs-lookup"><span data-stu-id="27593-113">_u_</span></span>
  
> <span data-ttu-id="27593-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="27593-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27593-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27593-115">Remarks</span></span>

<span data-ttu-id="27593-116">La macro **SizedDtblEdit** le permite definir un control de edición cuando se conoce el número de caracteres habilitados.</span><span class="sxs-lookup"><span data-stu-id="27593-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="27593-117">Se crea la nueva estructura con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="27593-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="27593-118">Para utilizar un puntero a la estructura resultante de la macro **SizedDtblEdit** como un puntero de estructura **DTBLEDIT** , realizar la conversión a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="27593-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="27593-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="27593-119">See also</span></span>

- [<span data-ttu-id="27593-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="27593-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="27593-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="27593-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

