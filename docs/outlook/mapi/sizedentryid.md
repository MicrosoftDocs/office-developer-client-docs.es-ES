---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 814cfeab61854469f460cc38f927b0e3723f6f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820680"
---
# <a name="sizedentryid"></a><span data-ttu-id="b5b0e-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="b5b0e-103">SizedENTRYID</span></span>

<span data-ttu-id="b5b0e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5b0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5b0e-105">Crea una estructura [ENTRYID](entryid.md) con nombre que contiene a un miembro **ab** de un tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="b5b0e-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5b0e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b5b0e-106">Header file:</span></span>  <br/> |<span data-ttu-id="b5b0e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5b0e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b5b0e-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="b5b0e-108">Related structure:</span></span>  <br/> |<span data-ttu-id="b5b0e-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="b5b0e-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="b5b0e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5b0e-110">Parameters</span></span>

<span data-ttu-id="b5b0e-111">__cb_</span><span class="sxs-lookup"><span data-stu-id="b5b0e-111">__cb_</span></span>
  
> <span data-ttu-id="b5b0e-112">Recuento de bytes en el miembro **ab** de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="b5b0e-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="b5b0e-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="b5b0e-113">__name_</span></span>
  
> <span data-ttu-id="b5b0e-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="b5b0e-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5b0e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5b0e-115">Remarks</span></span>

<span data-ttu-id="b5b0e-116">La macro **SizedENTRYID** le permite definir un identificador de entrada después de que se conocen los requisitos de longitud de la matriz.</span><span class="sxs-lookup"><span data-stu-id="b5b0e-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="b5b0e-117">Use esta macro para crear un identificador de entrada con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="b5b0e-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="b5b0e-118">Para usar la nueva estructura que el resultado de la macro **SizedENTRYID** como un puntero a una estructura de la **propiedad ENTRYID** , realice la conversión de tipos siguiente:</span><span class="sxs-lookup"><span data-stu-id="b5b0e-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="b5b0e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5b0e-119">See also</span></span>

- [<span data-ttu-id="b5b0e-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b5b0e-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="b5b0e-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="b5b0e-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

