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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: fea2b496a34d7aa7f9469158fae14daf6a770608
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820686"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="53809-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="53809-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="53809-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53809-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53809-105">Crea una estructura con nombre que incluye una estructura [DTBLCOMBOBOX](dtblcombobox.md) para describir un control de cuadro combinado y el número máximo de caracteres que se puede escribir en el control de edición asociado.</span><span class="sxs-lookup"><span data-stu-id="53809-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53809-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="53809-106">Header file:</span></span>  <br/> |<span data-ttu-id="53809-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53809-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="53809-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="53809-108">Related structure:</span></span>  <br/> |<span data-ttu-id="53809-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="53809-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="53809-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53809-110">Parameters</span></span>

<span data-ttu-id="53809-111">_n_</span><span class="sxs-lookup"><span data-stu-id="53809-111">_n_</span></span>
  
> <span data-ttu-id="53809-112">Número de caracteres que se pueden escribir en el cuadro combinado de control de edición.</span><span class="sxs-lookup"><span data-stu-id="53809-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="53809-113">_u_</span><span class="sxs-lookup"><span data-stu-id="53809-113">_u_</span></span>
  
> <span data-ttu-id="53809-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="53809-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53809-115">Notas</span><span class="sxs-lookup"><span data-stu-id="53809-115">Remarks</span></span>

<span data-ttu-id="53809-116">La macro **SizedDtblComboBox** le permite definir un cuadro combinado cuando se conoce la longitud de la cadena de caracteres habilitado.</span><span class="sxs-lookup"><span data-stu-id="53809-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="53809-117">Se crea la nueva estructura con los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="53809-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="53809-118">Para utilizar un puntero a la estructura resultante de la macro **SizedDtblComboBox** como un puntero de estructura **DTBLCOMBOBOX** , realizar la conversión a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="53809-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="53809-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="53809-119">See also</span></span>

- [<span data-ttu-id="53809-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="53809-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="53809-121">Macros relacionadas con las estructuras</span><span class="sxs-lookup"><span data-stu-id="53809-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

