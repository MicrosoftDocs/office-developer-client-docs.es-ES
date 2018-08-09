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
ms.openlocfilehash: 2a20f0f48eebe2194bc92afb98a620f9b39bb88d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817489"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="aed13-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="aed13-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="aed13-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aed13-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aed13-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de objeto de soporte técnico anterior.</span><span class="sxs-lookup"><span data-stu-id="aed13-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="aed13-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aed13-106">Parameters</span></span>

 <span data-ttu-id="aed13-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="aed13-107">_hResult_</span></span>
  
> <span data-ttu-id="aed13-108">[entrada] Un identificador para el valor de error generado en la llamada al método anterior para el objeto de soporte.</span><span class="sxs-lookup"><span data-stu-id="aed13-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="aed13-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aed13-109">_ulFlags_</span></span>
  
> <span data-ttu-id="aed13-110">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="aed13-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="aed13-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="aed13-111">The following flag can be set:</span></span>
    
<span data-ttu-id="aed13-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="aed13-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="aed13-113">Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="aed13-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="aed13-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="aed13-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="aed13-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="aed13-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="aed13-116">[out] Un puntero a un puntero a la estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="aed13-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="aed13-117">El parámetro _lppMAPIError_ se puede establecer en NULL si no se puede proporcionar una estructura **MAPIERROR** con información de error apropiado.</span><span class="sxs-lookup"><span data-stu-id="aed13-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="aed13-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aed13-118">Return value</span></span>

<span data-ttu-id="aed13-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="aed13-119">S_OK</span></span> 
  
> <span data-ttu-id="aed13-120">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="aed13-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="aed13-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="aed13-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="aed13-122">Se ha establecido el indicador MAPI_UNICODE y MAPI no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y MAPI admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="aed13-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aed13-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aed13-123">Remarks</span></span>

<span data-ttu-id="aed13-124">El método **IMAPISupport::GetLastError** se implementa para todos los objetos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="aed13-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="aed13-125">Los autores de llamadas pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="aed13-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aed13-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="aed13-126">Notes to callers</span></span>

<span data-ttu-id="aed13-127">Puede usar el puntero a la estructura **MAPIERROR** , si MAPI proporciona uno, en el parámetro _lppMAPIError_ sólo si **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="aed13-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="aed13-128">En ocasiones, MAPI no puede determinar cuál era el último error o no tiene nada más para informe sobre el error.</span><span class="sxs-lookup"><span data-stu-id="aed13-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="aed13-129">En esta situación, _lppMAPIError_ devuelve un puntero a NULL en su lugar.</span><span class="sxs-lookup"><span data-stu-id="aed13-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="aed13-130">Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="aed13-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="aed13-131">Para liberar toda la memoria asignada por MAPI, llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para la estructura **MAPIERROR** devuelta.</span><span class="sxs-lookup"><span data-stu-id="aed13-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aed13-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="aed13-132">See also</span></span>



[<span data-ttu-id="aed13-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="aed13-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="aed13-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="aed13-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="aed13-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="aed13-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="aed13-136">MAPI extendida de errores</span><span class="sxs-lookup"><span data-stu-id="aed13-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

