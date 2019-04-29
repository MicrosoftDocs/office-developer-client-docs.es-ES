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
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437647"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="1877c-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="1877c-103">SizedDtblEdit</span></span>

<span data-ttu-id="1877c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1877c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1877c-105">Crea una estructura con nombre que incluye una estructura [DTBLEDIT](dtbledit.md) para describir un control de edición y el número máximo de caracteres que se pueden escribir en el control.</span><span class="sxs-lookup"><span data-stu-id="1877c-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1877c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1877c-106">Header file:</span></span>  <br/> |<span data-ttu-id="1877c-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1877c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1877c-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="1877c-108">Related structure:</span></span>  <br/> |<span data-ttu-id="1877c-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="1877c-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="1877c-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="1877c-110">Parameters</span></span>

<span data-ttu-id="1877c-111">_n_</span><span class="sxs-lookup"><span data-stu-id="1877c-111">_n_</span></span>
  
> <span data-ttu-id="1877c-112">Número máximo de caracteres que se pueden escribir en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="1877c-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="1877c-113">_s_</span><span class="sxs-lookup"><span data-stu-id="1877c-113">_u_</span></span>
  
> <span data-ttu-id="1877c-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="1877c-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1877c-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1877c-115">Remarks</span></span>

<span data-ttu-id="1877c-116">La macro **SizedDtblEdit** permite definir un control de edición cuando se conoce el número de caracteres habilitados.</span><span class="sxs-lookup"><span data-stu-id="1877c-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="1877c-117">La nueva estructura se crea con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="1877c-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="1877c-118">Para usar un puntero a la estructura resultante desde la macro **SizedDtblEdit** como un puntero de estructura **DTBLEDIT** , realice la siguiente conversión:</span><span class="sxs-lookup"><span data-stu-id="1877c-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="1877c-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="1877c-119">See also</span></span>

- [<span data-ttu-id="1877c-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="1877c-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="1877c-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="1877c-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

