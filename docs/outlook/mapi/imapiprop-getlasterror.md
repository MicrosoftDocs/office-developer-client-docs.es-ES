---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342052"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="bab7c-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="bab7c-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="bab7c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bab7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bab7c-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior.</span><span class="sxs-lookup"><span data-stu-id="bab7c-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="bab7c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="bab7c-106">Parameters</span></span>

 <span data-ttu-id="bab7c-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="bab7c-107">_hResult_</span></span>
  
> <span data-ttu-id="bab7c-108">a Identificador del código de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="bab7c-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="bab7c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bab7c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="bab7c-110">a Máscara de máscara de marcadores que indica el formato del texto devuelto en la estructura **MAPIERROR** apuntado por _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="bab7c-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="bab7c-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="bab7c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="bab7c-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bab7c-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bab7c-113">Las cadenas deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="bab7c-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="bab7c-114">Si no se establece la marca MAPI_UNICODE, las cadenas deben estar en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="bab7c-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="bab7c-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="bab7c-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="bab7c-116">contempla Un puntero a un puntero a la estructura **MAPIERROR** que contiene información sobre la versión, el componente y el contexto del error.</span><span class="sxs-lookup"><span data-stu-id="bab7c-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="bab7c-117">El parámetro _lppMAPIError_ puede establecerse en NULL si no hay información de error que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="bab7c-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bab7c-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bab7c-118">Return value</span></span>

<span data-ttu-id="bab7c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="bab7c-119">S_OK</span></span> 
  
> <span data-ttu-id="bab7c-120">Se devolvió la información del error.</span><span class="sxs-lookup"><span data-stu-id="bab7c-120">The error information was returned.</span></span>
    
<span data-ttu-id="bab7c-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="bab7c-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="bab7c-122">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="bab7c-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bab7c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bab7c-123">Remarks</span></span>

<span data-ttu-id="bab7c-124">El método **IMAPIProp:: GetLastError** proporciona información sobre una llamada a un método anterior que produjo un error.</span><span class="sxs-lookup"><span data-stu-id="bab7c-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="bab7c-125">Los clientes pueden proporcionar a sus usuarios información detallada acerca del error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bab7c-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="bab7c-126">Todas las implementaciones de **GetLastError** que proporciona MAPI son implementaciones ANSI, excepto para la implementación de [IAddrBook](iaddrbookimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="bab7c-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="bab7c-127">El método **GetLastError** incluido con **IAddrBook** admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="bab7c-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bab7c-128">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="bab7c-128">Notes to implementers</span></span>

<span data-ttu-id="bab7c-129">Los detalles de la implementación de este método por un proveedor de transporte remoto y los mensajes que devuelve este método son para el proveedor de transporte, ya que las condiciones de error específicas que conducen a varios valores HRESULT serán diferentes para el transporte diferente. doctores.</span><span class="sxs-lookup"><span data-stu-id="bab7c-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="bab7c-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="bab7c-130">Notes to callers</span></span>

<span data-ttu-id="bab7c-131">Puede usar la estructura **MAPIERROR** apuntado por el parámetro _LppMAPIError_ , si **GetLastError** sólo proporciona uno, solo si el valor devuelto es S_OK.</span><span class="sxs-lookup"><span data-stu-id="bab7c-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="bab7c-132">A veces, **GetLastError** no puede determinar qué ha sido el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="bab7c-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="bab7c-133">En esta situación, un puntero a NULL se devuelve en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="bab7c-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="bab7c-134">Para liberar la memoria de la estructura **MAPIERROR** , llame a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="bab7c-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="bab7c-135">Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="bab7c-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bab7c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="bab7c-136">See also</span></span>



[<span data-ttu-id="bab7c-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bab7c-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="bab7c-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="bab7c-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="bab7c-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bab7c-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bab7c-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bab7c-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="bab7c-141">Errores extendidos de MAPI</span><span class="sxs-lookup"><span data-stu-id="bab7c-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

