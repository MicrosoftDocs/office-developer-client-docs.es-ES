---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416268"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="2dedf-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="2dedf-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="2dedf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dedf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dedf-105">Crea una estructura con nombre que incluye una estructura [DTBLCOMBOBOX](dtblcombobox.md) para describir un control de cuadro combinado y el número máximo de caracteres que se pueden escribir en el control de edición asociado.</span><span class="sxs-lookup"><span data-stu-id="2dedf-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2dedf-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2dedf-106">Header file:</span></span>  <br/> |<span data-ttu-id="2dedf-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2dedf-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2dedf-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="2dedf-108">Related structure:</span></span>  <br/> |<span data-ttu-id="2dedf-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="2dedf-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="2dedf-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="2dedf-110">Parameters</span></span>

<span data-ttu-id="2dedf-111">_n_</span><span class="sxs-lookup"><span data-stu-id="2dedf-111">_n_</span></span>
  
> <span data-ttu-id="2dedf-112">Número de caracteres que se pueden escribir en el control de edición del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="2dedf-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="2dedf-113">_s_</span><span class="sxs-lookup"><span data-stu-id="2dedf-113">_u_</span></span>
  
> <span data-ttu-id="2dedf-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="2dedf-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2dedf-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2dedf-115">Remarks</span></span>

<span data-ttu-id="2dedf-116">La macro **SizedDtblComboBox** permite definir un cuadro combinado cuando se conoce la longitud de la cadena de caracteres habilitada.</span><span class="sxs-lookup"><span data-stu-id="2dedf-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="2dedf-117">La nueva estructura se crea con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="2dedf-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="2dedf-118">Para usar un puntero a la estructura resultante desde la macro **SizedDtblComboBox** como un puntero de estructura **DTBLCOMBOBOX** , realice la siguiente conversión:</span><span class="sxs-lookup"><span data-stu-id="2dedf-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="2dedf-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="2dedf-119">See also</span></span>

- [<span data-ttu-id="2dedf-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="2dedf-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="2dedf-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="2dedf-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

