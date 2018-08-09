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
ms.openlocfilehash: e7a4fde57515f0b8a41b9acf4adb01dd177a7a19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816545"
---
# <a name="checkparms"></a><span data-ttu-id="9caee-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="9caee-103">CheckParms</span></span>

  
  
<span data-ttu-id="9caee-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9caee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9caee-105">Llama a una función interna para validar parámetros de depuración en los métodos de proveedor de servicio llamados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="9caee-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9caee-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9caee-106">Header file:</span></span>  <br/> |<span data-ttu-id="9caee-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="9caee-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="9caee-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="9caee-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9caee-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9caee-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9caee-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9caee-110">Called by:</span></span>  <br/> |<span data-ttu-id="9caee-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="9caee-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="9caee-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9caee-112">Parameters</span></span>

 <span data-ttu-id="9caee-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="9caee-113">_eMethod_</span></span>
  
> <span data-ttu-id="9caee-114">[entrada] Especifica el (enumeración), el método para validar.</span><span class="sxs-lookup"><span data-stu-id="9caee-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="9caee-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="9caee-115">_First_</span></span>
  
> <span data-ttu-id="9caee-116">[entrada] Puntero al primer argumento en la pila.</span><span class="sxs-lookup"><span data-stu-id="9caee-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9caee-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9caee-117">Return value</span></span>

<span data-ttu-id="9caee-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9caee-118">S_OK</span></span> 
  
> <span data-ttu-id="9caee-119">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="9caee-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9caee-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9caee-120">Remarks</span></span>

<span data-ttu-id="9caee-121">A diferencia de las macros [ValidateParms](validateparms.md) y [UlValidateParms](ulvalidateparms.md) , la macro **CheckParms** no realiza una validación del parámetro completa.</span><span class="sxs-lookup"><span data-stu-id="9caee-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="9caee-122">Parámetros pasados entre MAPI y servicio se supone que los proveedores de ser correcta, por lo que **CheckParms** realiza solo una validación de depuración.</span><span class="sxs-lookup"><span data-stu-id="9caee-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

