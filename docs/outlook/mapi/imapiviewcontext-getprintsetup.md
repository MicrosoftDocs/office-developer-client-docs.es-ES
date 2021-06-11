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
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425130"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="99ef2-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="99ef2-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="99ef2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99ef2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99ef2-105">Recupera la información de impresión actual.</span><span class="sxs-lookup"><span data-stu-id="99ef2-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="99ef2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="99ef2-106">Parameters</span></span>

 <span data-ttu-id="99ef2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99ef2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="99ef2-108">[in] Máscara de bits de marcas que controla el tipo de las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="99ef2-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="99ef2-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="99ef2-109">The following flag can be set:</span></span>
    
<span data-ttu-id="99ef2-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="99ef2-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="99ef2-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="99ef2-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="99ef2-112">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="99ef2-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="99ef2-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="99ef2-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="99ef2-114">[salida] Puntero a un puntero a una estructura que contiene la información de impresión.</span><span class="sxs-lookup"><span data-stu-id="99ef2-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99ef2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99ef2-115">Return value</span></span>

<span data-ttu-id="99ef2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="99ef2-116">S_OK</span></span> 
  
> <span data-ttu-id="99ef2-117">La información de impresión se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="99ef2-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99ef2-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99ef2-118">Remarks</span></span>

<span data-ttu-id="99ef2-119">Los objetos Form llaman al método **IMAPIViewContext::GetPrintSetup** para recuperar información sobre la instalación de la impresora antes de intentar imprimir el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="99ef2-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="99ef2-120">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="99ef2-120">Notes to implementers</span></span>

<span data-ttu-id="99ef2-121">Asigne los **miembros hDevMode** y **hDevName** de la estructura [FORMPRINTSETUP](formprintsetup.md) mediante la función Win32 **GlobalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="99ef2-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="99ef2-122">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="99ef2-122">Notes to callers</span></span>

<span data-ttu-id="99ef2-123">Si espera que los miembros **hDevMode** y **hDevName** de la estructura **FORMPRINTSETUP** que apunta el parámetro  _lppFormPrintSetup_ sean cadenas Unicode, establezca  _ulFlags_ en MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="99ef2-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="99ef2-124">De lo contrario, **GetPrintSetup** devolverá estas cadenas en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="99ef2-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="99ef2-125">Libera los **miembros hDevMode** y **hDevName** de la estructura **FORMPRINTSETUP** llamando a la función Win32 **GlobalFree**.</span><span class="sxs-lookup"><span data-stu-id="99ef2-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="99ef2-126">Libera toda la **estructura FORMPRINTSETUP** llamando a [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="99ef2-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99ef2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="99ef2-127">See also</span></span>



[<span data-ttu-id="99ef2-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="99ef2-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="99ef2-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="99ef2-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

