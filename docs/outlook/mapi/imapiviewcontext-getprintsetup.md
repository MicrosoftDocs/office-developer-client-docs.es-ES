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
ms.openlocfilehash: 63e3eca4e91e560a28d57f05250264d7e0592142
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587260"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="0c939-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="0c939-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="0c939-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c939-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c939-105">Recupera información de impresión actual.</span><span class="sxs-lookup"><span data-stu-id="0c939-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="0c939-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="0c939-106">Parameters</span></span>

 <span data-ttu-id="0c939-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c939-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0c939-108">[entrada] Máscara de bits de indicadores que controla el tipo de las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="0c939-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="0c939-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="0c939-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0c939-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="0c939-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0c939-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0c939-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="0c939-112">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0c939-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="0c939-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="0c939-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="0c939-114">[out] Puntero a un puntero a una estructura que contiene la información de impresión.</span><span class="sxs-lookup"><span data-stu-id="0c939-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c939-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c939-115">Return value</span></span>

<span data-ttu-id="0c939-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c939-116">S_OK</span></span> 
  
> <span data-ttu-id="0c939-117">La información de impresión se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0c939-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c939-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0c939-118">Remarks</span></span>

<span data-ttu-id="0c939-119">Objetos de formulario llamar al método **IMAPIViewContext::GetPrintSetup** para recuperar información acerca de la configuración de la impresora antes de intentar imprimir el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="0c939-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0c939-120">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="0c939-120">Notes to implementers</span></span>

<span data-ttu-id="0c939-121">Asignar a los miembros **hDevMode** y **hDevName** de la estructura [FORMPRINTSETUP](formprintsetup.md) mediante la función de Win32 **GlobalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="0c939-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0c939-122">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="0c939-122">Notes to callers</span></span>

<span data-ttu-id="0c939-123">Si se prevé la **hDevMode** y **hDevName** miembros de la estructura **FORMPRINTSETUP** indicada por el parámetro _lppFormPrintSetup_ como cadenas Unicode, establezca _ulFlags_ en MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="0c939-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="0c939-124">De lo contrario, **GetPrintSetup** devolverá estas cadenas en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0c939-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="0c939-125">Libere a los miembros **hDevMode** y **hDevName** de la estructura **FORMPRINTSETUP** mediante una llamada a la función de Win32 **GlobalFree**.</span><span class="sxs-lookup"><span data-stu-id="0c939-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="0c939-126">Libere toda la estructura **FORMPRINTSETUP** mediante una llamada [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="0c939-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c939-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0c939-127">See also</span></span>



[<span data-ttu-id="0c939-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="0c939-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="0c939-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c939-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

