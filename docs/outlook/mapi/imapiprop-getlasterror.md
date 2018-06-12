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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 67aa5b3d85de3df659b5aa1a351ec0d1dcf90248
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817404"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="8c60e-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8c60e-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="8c60e-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c60e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c60e-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior.</span><span class="sxs-lookup"><span data-stu-id="8c60e-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="8c60e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c60e-106">Parameters</span></span>

 <span data-ttu-id="8c60e-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="8c60e-107">_hResult_</span></span>
  
> <span data-ttu-id="8c60e-108">[entrada] Un identificador para el código de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="8c60e-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="8c60e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8c60e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8c60e-110">[entrada] Una máscara de bits de marcadores que indica el formato para el texto devuelto en la estructura **MAPIERROR** que señala _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="8c60e-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="8c60e-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="8c60e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="8c60e-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="8c60e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8c60e-113">Las cadenas deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="8c60e-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="8c60e-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas deben estar en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="8c60e-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="8c60e-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="8c60e-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="8c60e-116">[out] Un puntero a un puntero a la estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="8c60e-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="8c60e-117">El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ninguna información de error que devolver.</span><span class="sxs-lookup"><span data-stu-id="8c60e-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8c60e-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c60e-118">Return value</span></span>

<span data-ttu-id="8c60e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c60e-119">S_OK</span></span> 
  
> <span data-ttu-id="8c60e-120">Se devuelve la información de error.</span><span class="sxs-lookup"><span data-stu-id="8c60e-120">The error information was returned.</span></span>
    
<span data-ttu-id="8c60e-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8c60e-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8c60e-122">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="8c60e-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c60e-123">Notas</span><span class="sxs-lookup"><span data-stu-id="8c60e-123">Remarks</span></span>

<span data-ttu-id="8c60e-124">El método **IMAPIProp::GetLastError** proporciona información acerca de una llamada de método anteriores que no se pudo.</span><span class="sxs-lookup"><span data-stu-id="8c60e-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="8c60e-125">Los clientes pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8c60e-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="8c60e-126">Todas las implementaciones de **GetLastError** proporcionado por MAPI son implementaciones de ANSI, excepto para la implementación de [IAddrBook](iaddrbookimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="8c60e-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="8c60e-127">El método **GetLastError** incluido con **IAddrBook** es compatible con Unicode.</span><span class="sxs-lookup"><span data-stu-id="8c60e-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8c60e-128">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="8c60e-128">Notes to implementers</span></span>

<span data-ttu-id="8c60e-129">Los detalles de un control remoto de transporte del proveedor de implementación de este método y ¿cuáles son los mensajes de que este método devuelve hasta el proveedor de transporte, debido a que las condiciones de error concretos que conducen a distintos valores HRESULT será diferentes para el transporte diferente proveedores.</span><span class="sxs-lookup"><span data-stu-id="8c60e-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8c60e-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="8c60e-130">Notes to callers</span></span>

<span data-ttu-id="8c60e-131">Puede usar la estructura **MAPIERROR** indicada por el parámetro _lppMAPIError_ , si **GetLastError** proporciona uno, sólo si el valor devuelto es S_OK.</span><span class="sxs-lookup"><span data-stu-id="8c60e-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="8c60e-132">A veces **GetLastError** no puede determinar qué era el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="8c60e-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="8c60e-133">En esta situación, se devuelve un puntero a NULL en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8c60e-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="8c60e-134">Para liberar la memoria para la estructura **MAPIERROR** , llame a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8c60e-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="8c60e-135">Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="8c60e-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c60e-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="8c60e-136">See also</span></span>



[<span data-ttu-id="8c60e-137">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8c60e-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="8c60e-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="8c60e-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="8c60e-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8c60e-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8c60e-140">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c60e-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="8c60e-141">MAPI extendida de errores</span><span class="sxs-lookup"><span data-stu-id="8c60e-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

