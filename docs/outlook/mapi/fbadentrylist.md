---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: aae2e97b987414fc5e46b410465d3232b61f1ffe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816783"
---
# <a name="fbadentrylist"></a><span data-ttu-id="d509a-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="d509a-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="d509a-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d509a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d509a-105">Valida una lista de identificadores de entrada MAPI.</span><span class="sxs-lookup"><span data-stu-id="d509a-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d509a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d509a-106">Header file:</span></span>  <br/> |<span data-ttu-id="d509a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d509a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d509a-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="d509a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d509a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d509a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d509a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d509a-110">Called by:</span></span>  <br/> |<span data-ttu-id="d509a-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d509a-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="d509a-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d509a-112">Parameters</span></span>

 <span data-ttu-id="d509a-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="d509a-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="d509a-114">[entrada] Puntero a una estructura [ENTRYLIST](entrylist.md) que contiene una matriz de identificadores de entrada que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="d509a-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d509a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d509a-115">Return value</span></span>

<span data-ttu-id="d509a-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="d509a-116">TRUE</span></span> 
  
> <span data-ttu-id="d509a-117">Uno o varios de los identificadores de entrada listada no son válidos.</span><span class="sxs-lookup"><span data-stu-id="d509a-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="d509a-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="d509a-118">FALSE</span></span> 
  
> <span data-ttu-id="d509a-119">Todos los identificadores de entrada enumerados son válidos.</span><span class="sxs-lookup"><span data-stu-id="d509a-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d509a-120">Notas</span><span class="sxs-lookup"><span data-stu-id="d509a-120">Remarks</span></span>

<span data-ttu-id="d509a-121">La función **FBadEntryList** determina si se ha generado correctamente la lista de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d509a-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="d509a-122">Un ejemplo de un identificador no válido es uno para qué memoria se ha asignado incorrectamente o un identificador de un tamaño incorrecto.</span><span class="sxs-lookup"><span data-stu-id="d509a-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

