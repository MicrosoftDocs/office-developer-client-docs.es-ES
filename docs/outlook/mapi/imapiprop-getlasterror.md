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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435834"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="640fc-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="640fc-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="640fc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="640fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="640fc-105">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior.</span><span class="sxs-lookup"><span data-stu-id="640fc-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="640fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="640fc-106">Parameters</span></span>

 <span data-ttu-id="640fc-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="640fc-107">_hResult_</span></span>
  
> <span data-ttu-id="640fc-108">[entrada] Identificador del código de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="640fc-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="640fc-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="640fc-109">_ulFlags_</span></span>
  
> <span data-ttu-id="640fc-110">[entrada] Máscara de bits de marcas que indica el formato del texto devuelto en la estructura **MAPIERROR** a la que  _apunta lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="640fc-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="640fc-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="640fc-111">The following flag can be set:</span></span>
    
<span data-ttu-id="640fc-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="640fc-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="640fc-113">Las cadenas deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="640fc-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="640fc-114">Si no MAPI_UNICODE marca, las cadenas deben estar en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="640fc-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="640fc-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="640fc-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="640fc-116">[salida] Puntero a un puntero a la estructura **MAPIERROR** que contiene información de versión, componente y contexto del error.</span><span class="sxs-lookup"><span data-stu-id="640fc-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="640fc-117">El  _parámetro lppMAPIError_ se puede establecer en NULL si no hay información de error que devolver.</span><span class="sxs-lookup"><span data-stu-id="640fc-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="640fc-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="640fc-118">Return value</span></span>

<span data-ttu-id="640fc-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="640fc-119">S_OK</span></span> 
  
> <span data-ttu-id="640fc-120">Se ha devuelto la información de error.</span><span class="sxs-lookup"><span data-stu-id="640fc-120">The error information was returned.</span></span>
    
<span data-ttu-id="640fc-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="640fc-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="640fc-122">Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="640fc-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="640fc-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="640fc-123">Remarks</span></span>

<span data-ttu-id="640fc-124">El **método IMAPIProp::GetLastError** proporciona información acerca de una llamada de método anterior que ha fallado.</span><span class="sxs-lookup"><span data-stu-id="640fc-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="640fc-125">Los clientes pueden proporcionar a sus usuarios información detallada sobre el error incluyendo los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="640fc-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="640fc-126">Todas las implementaciones de **GetLastError** proporcionadas por MAPI son implementaciones ANSI, excepto para la implementación [de IAddrBook.](iaddrbookimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="640fc-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="640fc-127">El **método GetLastError** incluido con **IAddrBook admite** Unicode.</span><span class="sxs-lookup"><span data-stu-id="640fc-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="640fc-128">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="640fc-128">Notes to implementers</span></span>

<span data-ttu-id="640fc-129">Los detalles de la implementación de este método por parte de un proveedor de transporte remoto y los mensajes que devuelve este método están en función del proveedor de transporte, ya que las condiciones de error concretas que llevan a varios valores HRESULT serán diferentes para distintos proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="640fc-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="640fc-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="640fc-130">Notes to callers</span></span>

<span data-ttu-id="640fc-131">Puede usar la estructura **MAPIERROR** a la que apunta el parámetro  _lppMAPIError,_ si **GetLastError** proporciona uno, solo si el valor devuelto es S_OK.</span><span class="sxs-lookup"><span data-stu-id="640fc-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="640fc-132">A **veces, GetLastError** no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="640fc-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="640fc-133">En esta situación, se devuelve un puntero a NULL  _en lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="640fc-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="640fc-134">Para liberar la memoria de la **estructura MAPIERROR,** llame a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="640fc-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="640fc-135">Para obtener más información acerca **del método GetLastError,** vea [errores extendidos de MAPI.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="640fc-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="640fc-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="640fc-136">See also</span></span>



[<span data-ttu-id="640fc-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="640fc-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="640fc-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="640fc-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="640fc-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="640fc-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="640fc-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="640fc-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="640fc-141">Errores extendidos de MAPI</span><span class="sxs-lookup"><span data-stu-id="640fc-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

