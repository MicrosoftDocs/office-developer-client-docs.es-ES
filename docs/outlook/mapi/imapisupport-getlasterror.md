---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438550"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="d496e-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d496e-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="d496e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d496e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d496e-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior del objeto support.</span><span class="sxs-lookup"><span data-stu-id="d496e-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="d496e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d496e-106">Parameters</span></span>

 <span data-ttu-id="d496e-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="d496e-107">_hResult_</span></span>
  
> <span data-ttu-id="d496e-108">a Identificador del valor de error generado en la llamada al método anterior para el objeto de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="d496e-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="d496e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d496e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d496e-110">a Máscara de máscara de marcadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="d496e-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="d496e-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="d496e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d496e-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d496e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d496e-113">Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d496e-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="d496e-114">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d496e-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="d496e-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="d496e-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="d496e-116">contempla Un puntero a un puntero a la estructura **MAPIERROR** que contiene información sobre la versión, el componente y el contexto del error.</span><span class="sxs-lookup"><span data-stu-id="d496e-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="d496e-117">El parámetro _lppMAPIError_ puede establecerse en NULL si no se puede proporcionar una estructura **MAPIERROR** con información de error adecuada.</span><span class="sxs-lookup"><span data-stu-id="d496e-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d496e-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d496e-118">Return value</span></span>

<span data-ttu-id="d496e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d496e-119">S_OK</span></span> 
  
> <span data-ttu-id="d496e-120">La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="d496e-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="d496e-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d496e-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d496e-122">Se estableció la marca MAPI_UNICODE y MAPI no admite Unicode, o bien no se estableció MAPI_UNICODE y MAPI solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="d496e-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d496e-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d496e-123">Remarks</span></span>

<span data-ttu-id="d496e-124">El método **IMAPISupport:: GetLastError** se implementa para todos los objetos de soporte.</span><span class="sxs-lookup"><span data-stu-id="d496e-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="d496e-125">Los autores de llamadas pueden proporcionar a sus usuarios información detallada acerca del error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d496e-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d496e-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d496e-126">Notes to callers</span></span>

<span data-ttu-id="d496e-127">Puede usar el puntero a la estructura **MAPIERROR** , si MAPI proporciona uno, en el parámetro _LppMAPIError_ solo si **GetLastError** Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="d496e-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="d496e-128">A veces MAPI no puede determinar cuál era el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="d496e-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="d496e-129">En esta situación, _lppMAPIError_ devuelve un puntero a NULL en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d496e-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="d496e-130">Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="d496e-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="d496e-131">Para liberar toda la memoria asignada por MAPI, llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para la estructura **MAPIERROR** devuelta.</span><span class="sxs-lookup"><span data-stu-id="d496e-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d496e-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="d496e-132">See also</span></span>



[<span data-ttu-id="d496e-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d496e-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d496e-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d496e-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d496e-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d496e-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="d496e-136">Errores extendidos de MAPI</span><span class="sxs-lookup"><span data-stu-id="d496e-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

