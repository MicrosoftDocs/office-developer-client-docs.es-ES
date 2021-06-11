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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427776"
---
# <a name="fbadentrylist"></a><span data-ttu-id="426c0-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="426c0-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="426c0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="426c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="426c0-105">Valida una lista de identificadores de entrada MAPI.</span><span class="sxs-lookup"><span data-stu-id="426c0-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="426c0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="426c0-106">Header file:</span></span>  <br/> |<span data-ttu-id="426c0-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="426c0-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="426c0-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="426c0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="426c0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="426c0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="426c0-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="426c0-110">Called by:</span></span>  <br/> |<span data-ttu-id="426c0-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="426c0-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="426c0-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="426c0-112">Parameters</span></span>

 <span data-ttu-id="426c0-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="426c0-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="426c0-114">[in] Puntero a una [estructura ENTRYLIST](entrylist.md) que contiene una matriz de identificadores de entrada que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="426c0-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="426c0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="426c0-115">Return value</span></span>

<span data-ttu-id="426c0-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="426c0-116">TRUE</span></span> 
  
> <span data-ttu-id="426c0-117">Uno o varios de los identificadores de entrada enumerados no son válidos.</span><span class="sxs-lookup"><span data-stu-id="426c0-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="426c0-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="426c0-118">FALSE</span></span> 
  
> <span data-ttu-id="426c0-119">Todos los identificadores de entrada enumerados son válidos.</span><span class="sxs-lookup"><span data-stu-id="426c0-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="426c0-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="426c0-120">Remarks</span></span>

<span data-ttu-id="426c0-121">La **función FBadEntryList** determina si la lista de identificadores de entrada se ha generado correctamente.</span><span class="sxs-lookup"><span data-stu-id="426c0-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="426c0-122">Un ejemplo de un identificador no válido es uno para el que la memoria se ha asignado incorrectamente o un identificador de un tamaño incorrecto.</span><span class="sxs-lookup"><span data-stu-id="426c0-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

