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
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405712"
---
# <a name="sizedentryid"></a><span data-ttu-id="e1fe9-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="e1fe9-103">SizedENTRYID</span></span>

<span data-ttu-id="e1fe9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1fe9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1fe9-105">Crea una estructura [EntryID](entryid.md) con nombre que contiene un miembro **AB** de un tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="e1fe9-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1fe9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e1fe9-106">Header file:</span></span>  <br/> |<span data-ttu-id="e1fe9-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e1fe9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e1fe9-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="e1fe9-108">Related structure:</span></span>  <br/> |<span data-ttu-id="e1fe9-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="e1fe9-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="e1fe9-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1fe9-110">Parameters</span></span>

<span data-ttu-id="e1fe9-111">__CB_</span><span class="sxs-lookup"><span data-stu-id="e1fe9-111">__cb_</span></span>
  
> <span data-ttu-id="e1fe9-112">Número de bytes en el miembro **AB** de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="e1fe9-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="e1fe9-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="e1fe9-113">__name_</span></span>
  
> <span data-ttu-id="e1fe9-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="e1fe9-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1fe9-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1fe9-115">Remarks</span></span>

<span data-ttu-id="e1fe9-116">La macro **SizedENTRYID** permite definir un identificador de entrada después de conocer los requisitos de longitud de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e1fe9-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="e1fe9-117">Use esta macro para crear un identificador de entrada con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="e1fe9-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="e1fe9-118">Para usar la nueva estructura que resulta de la macro **SizedENTRYID** como un puntero a una estructura **EntryID** , realice la siguiente conversión:</span><span class="sxs-lookup"><span data-stu-id="e1fe9-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="e1fe9-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="e1fe9-119">See also</span></span>

- [<span data-ttu-id="e1fe9-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e1fe9-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="e1fe9-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="e1fe9-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

