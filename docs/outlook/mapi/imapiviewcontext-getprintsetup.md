---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 7fdf76bc56feb7e46370e7fcf66c55d229933eca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817634"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="600cd-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="600cd-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="600cd-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="600cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="600cd-105">Recupera información de impresión actual.</span><span class="sxs-lookup"><span data-stu-id="600cd-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="600cd-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="600cd-106">Parameters</span></span>

 <span data-ttu-id="600cd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="600cd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="600cd-108">[entrada] Máscara de bits de indicadores que controla el tipo de las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="600cd-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="600cd-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="600cd-109">The following flag can be set:</span></span>
    
<span data-ttu-id="600cd-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="600cd-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="600cd-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="600cd-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="600cd-112">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="600cd-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="600cd-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="600cd-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="600cd-114">[out] Puntero a un puntero a una estructura que contiene la información de impresión.</span><span class="sxs-lookup"><span data-stu-id="600cd-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="600cd-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="600cd-115">Return value</span></span>

<span data-ttu-id="600cd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="600cd-116">S_OK</span></span> 
  
> <span data-ttu-id="600cd-117">La información de impresión se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="600cd-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="600cd-118">Notas</span><span class="sxs-lookup"><span data-stu-id="600cd-118">Remarks</span></span>

<span data-ttu-id="600cd-119">Objetos de formulario llamar al método **IMAPIViewContext::GetPrintSetup** para recuperar información acerca de la configuración de la impresora antes de intentar imprimir el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="600cd-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="600cd-120">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="600cd-120">Notes to implementers</span></span>

<span data-ttu-id="600cd-121">Asignar a los miembros **hDevMode** y **hDevName** de la estructura [FORMPRINTSETUP](formprintsetup.md) mediante la función de Win32 **GlobalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="600cd-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="600cd-122">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="600cd-122">Notes to callers</span></span>

<span data-ttu-id="600cd-123">Si se prevé la **hDevMode** y **hDevName** miembros de la estructura **FORMPRINTSETUP** indicada por el parámetro _lppFormPrintSetup_ como cadenas Unicode, establezca _ulFlags_ en MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="600cd-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="600cd-124">De lo contrario, **GetPrintSetup** devolverá estas cadenas en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="600cd-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="600cd-125">Libere a los miembros **hDevMode** y **hDevName** de la estructura **FORMPRINTSETUP** mediante una llamada a la función de Win32 **GlobalFree**.</span><span class="sxs-lookup"><span data-stu-id="600cd-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="600cd-126">Libere toda la estructura **FORMPRINTSETUP** mediante una llamada [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="600cd-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="600cd-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="600cd-127">See also</span></span>



[<span data-ttu-id="600cd-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="600cd-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="600cd-129">IMAPIViewContext: IUnknown</span><span class="sxs-lookup"><span data-stu-id="600cd-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

