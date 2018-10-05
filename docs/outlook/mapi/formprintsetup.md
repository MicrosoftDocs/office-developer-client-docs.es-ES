---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386575"
---
# <a name="formprintsetup"></a><span data-ttu-id="a972d-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="a972d-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="a972d-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a972d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a972d-105">Se describe la información de configuración de impresión para el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="a972d-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a972d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a972d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a972d-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="a972d-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a><span data-ttu-id="a972d-108">Members</span><span class="sxs-lookup"><span data-stu-id="a972d-108">Members</span></span>

 <span data-ttu-id="a972d-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a972d-109">**ulFlags**</span></span>
  
> <span data-ttu-id="a972d-110">Máscara de bits de indicadores que controla el tipo de las cadenas.</span><span class="sxs-lookup"><span data-stu-id="a972d-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="a972d-111">Se puede usar la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="a972d-111">The following flag can be used:</span></span>
    
<span data-ttu-id="a972d-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="a972d-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a972d-113">Las cadenas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a972d-113">The strings are in Unicode format.</span></span> <span data-ttu-id="a972d-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a972d-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a972d-115">**hDevmode**</span><span class="sxs-lookup"><span data-stu-id="a972d-115">**hDevmode**</span></span>
  
> <span data-ttu-id="a972d-116">Controlar en el modo de la impresora.</span><span class="sxs-lookup"><span data-stu-id="a972d-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="a972d-117">**hDevnames**</span><span class="sxs-lookup"><span data-stu-id="a972d-117">**hDevnames**</span></span>
  
> <span data-ttu-id="a972d-118">Identificador de la ruta de acceso de la impresora.</span><span class="sxs-lookup"><span data-stu-id="a972d-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="a972d-119">**ulFirstPageNumber**</span><span class="sxs-lookup"><span data-stu-id="a972d-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="a972d-120">Número de página de la primera página que debe imprimirse.</span><span class="sxs-lookup"><span data-stu-id="a972d-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="a972d-121">**ulFPrintAttachments**</span><span class="sxs-lookup"><span data-stu-id="a972d-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="a972d-122">Marca que indica si hay datos adjuntos que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="a972d-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="a972d-123">Si hay datos adjuntos para imprimir, el miembro **ulFPrintAttachments** está establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="a972d-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="a972d-124">Si no hay ningún datos adjuntos para imprimir, se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="a972d-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a972d-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a972d-125">Remarks</span></span>

<span data-ttu-id="a972d-126">La estructura **FORMPRINTSETUP** se usa para describir la información de configuración de impresión de un objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="a972d-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="a972d-127">Las implementaciones de [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) rellene la estructura **FORMPRINTSETUP** y devuelven en el contenido del parámetro de salida _lppFormPrintSetup_ de **GetPrintSetup**.</span><span class="sxs-lookup"><span data-stu-id="a972d-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="a972d-128">Si el indicador MAPI_UNICODE se pasa en el parámetro _ulFlags_ de **GetPrintSetup**, las cadenas que se hace referencia a los miembros **hDevmode** y **hDevNames no** deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a972d-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="a972d-129">De lo contrario, las cadenas deberían estar en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a972d-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="a972d-130">Visores de formulario implementar **IMAPIViewContext** deben asignar la estructura **FORMPRINTSETUP** mediante la función de asignador MAPI [MAPIAllocateBuffer](mapiallocatebuffer.md), pero asignar a los miembros individuales, **hDevMode** y **hDevNames**, con la función de Windows [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span><span class="sxs-lookup"><span data-stu-id="a972d-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="a972d-131">La versión de memoria se administra de forma similar.</span><span class="sxs-lookup"><span data-stu-id="a972d-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="a972d-132">Los miembros **hDevMode** y **hDevNames no** se deben liberar mediante la función de Windows [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) mientras que la estructura **FORMPRINTSETUP** se debe liberar con la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a972d-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a972d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a972d-133">See also</span></span>



[<span data-ttu-id="a972d-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="a972d-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="a972d-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a972d-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a972d-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a972d-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="a972d-137">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="a972d-137">MAPI Structures</span></span>](mapi-structures.md)

