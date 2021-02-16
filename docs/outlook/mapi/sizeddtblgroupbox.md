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
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419320"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="99478-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="99478-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="99478-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99478-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99478-105">Crea una estructura con nombre que incluye una [estructura DTBLGROUPBOX](dtblgroupbox.md) para describir un control de cuadro de grupo y una etiqueta de una longitud especificada.</span><span class="sxs-lookup"><span data-stu-id="99478-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99478-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="99478-106">Header file:</span></span>  <br/> |<span data-ttu-id="99478-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99478-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="99478-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="99478-108">Related structure:</span></span>  <br/> |<span data-ttu-id="99478-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="99478-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="99478-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99478-110">Parameters</span></span>

<span data-ttu-id="99478-111">_n_</span><span class="sxs-lookup"><span data-stu-id="99478-111">_n_</span></span>
  
> <span data-ttu-id="99478-112">Longitud de la etiqueta del cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="99478-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="99478-113">_s_</span><span class="sxs-lookup"><span data-stu-id="99478-113">_u_</span></span>
  
> <span data-ttu-id="99478-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="99478-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99478-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99478-115">Remarks</span></span>

<span data-ttu-id="99478-116">La macro **SizedDtblGroupBox** permite definir un control de cuadro de grupo cuando se conoce la longitud de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="99478-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="99478-117">La nueva estructura se crea con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="99478-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="99478-118">Para usar un puntero a la estructura resultante de la macro **SizedDtblGroupBox** como puntero de estructura **DTBLGROUPBOX,** realice la conversión siguiente:</span><span class="sxs-lookup"><span data-stu-id="99478-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="99478-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="99478-119">See also</span></span>

- [<span data-ttu-id="99478-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="99478-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="99478-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="99478-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

