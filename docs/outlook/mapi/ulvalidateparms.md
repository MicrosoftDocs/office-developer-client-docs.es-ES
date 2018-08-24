---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b71d1f477435b4a9327b4156560d1aa2e6079536
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578706"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="c55c7-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="c55c7-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="c55c7-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c55c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c55c7-105">Llama a una función interna para comprobar si que las aplicaciones cliente de los parámetros han pasado a proveedores de servicios y MAPI.</span><span class="sxs-lookup"><span data-stu-id="c55c7-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c55c7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c55c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="c55c7-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c55c7-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c55c7-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="c55c7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c55c7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c55c7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c55c7-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c55c7-110">Called by:</span></span>  <br/> |<span data-ttu-id="c55c7-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c55c7-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="c55c7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c55c7-112">Parameters</span></span>

 <span data-ttu-id="c55c7-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="c55c7-113">_eMethod_</span></span>
  
> <span data-ttu-id="c55c7-114">[entrada] Especifica el (enumeración), el método para validar.</span><span class="sxs-lookup"><span data-stu-id="c55c7-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="c55c7-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="c55c7-115">_First_</span></span>
  
> <span data-ttu-id="c55c7-116">[entrada] Puntero al primer argumento en la pila.</span><span class="sxs-lookup"><span data-stu-id="c55c7-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c55c7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c55c7-117">Return value</span></span>

<span data-ttu-id="c55c7-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c55c7-118">S_OK</span></span> 
  
> <span data-ttu-id="c55c7-119">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="c55c7-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c55c7-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="c55c7-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="c55c7-121">Un error no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="c55c7-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c55c7-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c55c7-122">Remarks</span></span>

<span data-ttu-id="c55c7-123">Parámetros pasados entre MAPI y servicio proveedores se supone que sea correcta y se sincronizan sólo depuración validación con la macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="c55c7-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="c55c7-124">Proveedores deben comprobar todos los parámetros que se pasó por las aplicaciones cliente, pero los clientes deben se presupone que MAPI y proveedor de parámetros correctos.</span><span class="sxs-lookup"><span data-stu-id="c55c7-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="c55c7-125">Use la macro **HR_FAILED** para comprobar los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="c55c7-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="c55c7-126">La macro **UlValidateParms** se llama de manera diferente dependiendo de si el código de llamada es C o C++.</span><span class="sxs-lookup"><span data-stu-id="c55c7-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="c55c7-127">Esta macro se usa para validar los parámetros de los métodos de **IUnknown** y MAPI pocos que devuelven ULONG en lugar de los valores HRESULT; la macro [ValidateParms](validateparms.md) funciona para todos los demás.</span><span class="sxs-lookup"><span data-stu-id="c55c7-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

