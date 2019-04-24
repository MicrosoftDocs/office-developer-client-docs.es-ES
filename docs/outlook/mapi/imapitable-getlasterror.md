---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329004"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="3933b-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3933b-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="3933b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3933b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3933b-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3933b-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="3933b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3933b-106">Parameters</span></span>

 <span data-ttu-id="3933b-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="3933b-107">_hResult_</span></span>
  
> <span data-ttu-id="3933b-108">a HRESULT que contiene el error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="3933b-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="3933b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3933b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3933b-110">a Máscara de máscara de marcadores que controla el tipo de las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="3933b-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="3933b-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="3933b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3933b-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3933b-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3933b-113">Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="3933b-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="3933b-114">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="3933b-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="3933b-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="3933b-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="3933b-116">contempla Puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene la versión, el componente y la información de contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="3933b-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="3933b-117">El parámetro _lppMAPIError_ puede establecerse en NULL si no se puede proporcionar una estructura **MAPIERROR** con la información adecuada.</span><span class="sxs-lookup"><span data-stu-id="3933b-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3933b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3933b-118">Return value</span></span>

<span data-ttu-id="3933b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3933b-119">S_OK</span></span> 
  
> <span data-ttu-id="3933b-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="3933b-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3933b-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3933b-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3933b-122">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="3933b-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3933b-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3933b-123">Remarks</span></span>

<span data-ttu-id="3933b-124">El método **IMAPITable:: GetLastError** devuelve información detallada, si está disponible, sobre una llamada a un método anterior que produjo un error.</span><span class="sxs-lookup"><span data-stu-id="3933b-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="3933b-125">Esta información se puede mostrar en un mensaje o un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3933b-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3933b-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3933b-126">Notes to callers</span></span>

<span data-ttu-id="3933b-127">Llame a **GetLastError** siempre que necesite Mostrar información sobre un error al usuario.</span><span class="sxs-lookup"><span data-stu-id="3933b-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="3933b-128">Puede hacer uso de la estructura [MAPIERROR](mapierror.md) apuntado por el parámetro _lppMAPIError_ si el objeto Table proporciona solo uno si **GetLastError** Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="3933b-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="3933b-129">A veces, la implementación de la tabla no puede determinar qué último error ha sido o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="3933b-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="3933b-130">En esta situación, el puntero que se encuentra en _lppMAPIError_ se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="3933b-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="3933b-131">Para liberar toda la memoria asignada para la estructura **MAPIERROR** , llame a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="3933b-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="3933b-132">Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3933b-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3933b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3933b-133">See also</span></span>



[<span data-ttu-id="3933b-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="3933b-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="3933b-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3933b-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3933b-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3933b-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

