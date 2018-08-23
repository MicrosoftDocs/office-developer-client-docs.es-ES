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
ms.openlocfilehash: d797acdbf2abfb88151d69d0c93e743f07afc5c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563873"
---
# <a name="sizedentryid"></a><span data-ttu-id="fdc7f-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="fdc7f-103">SizedENTRYID</span></span>

<span data-ttu-id="fdc7f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdc7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdc7f-105">Crea una estructura [ENTRYID](entryid.md) con nombre que contiene a un miembro **ab** de un tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fdc7f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fdc7f-106">Header file:</span></span>  <br/> |<span data-ttu-id="fdc7f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fdc7f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fdc7f-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="fdc7f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="fdc7f-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="fdc7f-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="fdc7f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdc7f-110">Parameters</span></span>

<span data-ttu-id="fdc7f-111">__cb_</span><span class="sxs-lookup"><span data-stu-id="fdc7f-111">__cb_</span></span>
  
> <span data-ttu-id="fdc7f-112">Recuento de bytes en el miembro **ab** de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="fdc7f-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="fdc7f-113">__name_</span></span>
  
> <span data-ttu-id="fdc7f-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fdc7f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fdc7f-115">Remarks</span></span>

<span data-ttu-id="fdc7f-116">La macro **SizedENTRYID** le permite definir un identificador de entrada después de que se conocen los requisitos de longitud de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="fdc7f-117">Use esta macro para crear un identificador de entrada con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="fdc7f-118">Para usar la nueva estructura que el resultado de la macro **SizedENTRYID** como un puntero a una estructura de la **propiedad ENTRYID** , realice la conversión de tipos siguiente:</span><span class="sxs-lookup"><span data-stu-id="fdc7f-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="fdc7f-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fdc7f-119">See also</span></span>

- [<span data-ttu-id="fdc7f-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fdc7f-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="fdc7f-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="fdc7f-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

