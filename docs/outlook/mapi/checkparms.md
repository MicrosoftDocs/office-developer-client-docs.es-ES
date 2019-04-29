---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422281"
---
# <a name="checkparms"></a><span data-ttu-id="27efd-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="27efd-103">CheckParms</span></span>

  
  
<span data-ttu-id="27efd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27efd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27efd-105">Llama a una función interna para validar los parámetros de depuración de los métodos de proveedor de servicios a los que llama MAPI.</span><span class="sxs-lookup"><span data-stu-id="27efd-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27efd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="27efd-106">Header file:</span></span>  <br/> |<span data-ttu-id="27efd-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="27efd-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="27efd-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="27efd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="27efd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="27efd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="27efd-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="27efd-110">Called by:</span></span>  <br/> |<span data-ttu-id="27efd-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="27efd-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="27efd-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27efd-112">Parameters</span></span>

 <span data-ttu-id="27efd-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="27efd-113">_eMethod_</span></span>
  
> <span data-ttu-id="27efd-114">a Especifica, por enumeración, el método que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="27efd-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="27efd-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="27efd-115">_First_</span></span>
  
> <span data-ttu-id="27efd-116">a Puntero al primer argumento de la pila.</span><span class="sxs-lookup"><span data-stu-id="27efd-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="27efd-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27efd-117">Return value</span></span>

<span data-ttu-id="27efd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="27efd-118">S_OK</span></span> 
  
> <span data-ttu-id="27efd-119">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="27efd-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27efd-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27efd-120">Remarks</span></span>

<span data-ttu-id="27efd-121">A diferencia de las macros [ValidateParms](validateparms.md) y [UlValidateParms](ulvalidateparms.md) , la macro **CheckParms** no realiza una validación completa de parámetros.</span><span class="sxs-lookup"><span data-stu-id="27efd-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="27efd-122">Se supone que los parámetros que se han pasado entre MAPI y los proveedores de servicios son correctos, por lo que **CheckParms** solo realiza una validación de depuración.</span><span class="sxs-lookup"><span data-stu-id="27efd-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

