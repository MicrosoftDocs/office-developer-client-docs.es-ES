---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 882638d5359154a56fa4438e7a62f213159f916d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581219"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="27502-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="27502-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="27502-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27502-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27502-105">Crea una estructura con nombre que incluye una estructura [DTBLGROUPBOX](dtblgroupbox.md) para describir un control de cuadro de grupo y una etiqueta de un período especificado.</span><span class="sxs-lookup"><span data-stu-id="27502-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27502-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="27502-106">Header file:</span></span>  <br/> |<span data-ttu-id="27502-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27502-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="27502-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="27502-108">Related structure:</span></span>  <br/> |<span data-ttu-id="27502-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="27502-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="27502-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27502-110">Parameters</span></span>

<span data-ttu-id="27502-111">_n_</span><span class="sxs-lookup"><span data-stu-id="27502-111">_n_</span></span>
  
> <span data-ttu-id="27502-112">Longitud de etiqueta del cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="27502-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="27502-113">_s_</span><span class="sxs-lookup"><span data-stu-id="27502-113">_u_</span></span>
  
> <span data-ttu-id="27502-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="27502-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27502-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27502-115">Remarks</span></span>

<span data-ttu-id="27502-116">La macro **SizedDtblGroupBox** le permite definir un control de cuadro de grupo cuando se conoce la longitud de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="27502-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="27502-117">Se crea la nueva estructura con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="27502-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="27502-118">Para utilizar un puntero a la estructura resultante de la macro **SizedDtblGroupBox** como un puntero de estructura **DTBLGROUPBOX** , realizar la conversión a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="27502-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="27502-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="27502-119">See also</span></span>

- [<span data-ttu-id="27502-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="27502-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="27502-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="27502-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

