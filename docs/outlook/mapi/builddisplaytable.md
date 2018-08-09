---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b821394f32a938f4878ee93e685aafbeb0786597
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816517"
---
# <a name="builddisplaytable"></a><span data-ttu-id="57be2-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="57be2-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="57be2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="57be2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="57be2-105">Crea una tabla de presentación de datos de la página de propiedad contenidos en una o más estructuras [DTPAGE](dtpage.md) .</span><span class="sxs-lookup"><span data-stu-id="57be2-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57be2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="57be2-106">Header file:</span></span>  <br/> |<span data-ttu-id="57be2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="57be2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="57be2-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="57be2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="57be2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="57be2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="57be2-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="57be2-110">Called by:</span></span>  <br/> |<span data-ttu-id="57be2-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="57be2-111">Service providers</span></span>  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a><span data-ttu-id="57be2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57be2-112">Parameters</span></span>

 <span data-ttu-id="57be2-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="57be2-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="57be2-114">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="57be2-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="57be2-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="57be2-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="57be2-116">[entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="57be2-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="57be2-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="57be2-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="57be2-118">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="57be2-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="57be2-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="57be2-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="57be2-120">No usados; debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="57be2-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="57be2-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="57be2-121">_hInstance_</span></span>
  
> <span data-ttu-id="57be2-122">[entrada] Una instancia de un objeto MAPI desde la que **BuildDisplayTable** recupera los recursos.</span><span class="sxs-lookup"><span data-stu-id="57be2-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="57be2-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="57be2-123">_cPages_</span></span>
  
> <span data-ttu-id="57be2-124">[entrada] Recuento de las estructuras [DTPAGE](dtpage.md) en la matriz indicada por el parámetro _lpPage_ .</span><span class="sxs-lookup"><span data-stu-id="57be2-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="57be2-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="57be2-125">_lpPage_</span></span>
  
> <span data-ttu-id="57be2-126">[entrada] Puntero a una matriz de estructuras **DTPAGE** que contienen información acerca de las páginas de la tabla para mostrar que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="57be2-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="57be2-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57be2-127">_ulFlags_</span></span>
  
> <span data-ttu-id="57be2-128">[entrada] Máscara de bits de indicadores.</span><span class="sxs-lookup"><span data-stu-id="57be2-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="57be2-129">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="57be2-129">The following flag can be set:</span></span>
    
<span data-ttu-id="57be2-130">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="57be2-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="57be2-131">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="57be2-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="57be2-132">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="57be2-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="57be2-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="57be2-133">_lppTable_</span></span>
  
> <span data-ttu-id="57be2-134">[out] Puntero a un puntero a la tabla para mostrar, que expone la interfaz [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="57be2-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="57be2-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="57be2-135">_lppTblData_</span></span>
  
> <span data-ttu-id="57be2-136">[entrada, salida] Puntero a un puntero a un objeto de datos de tabla expone la interfaz [ITableData](itabledataiunknown.md) en la tabla devuelta en el parámetro _lppTable_ .</span><span class="sxs-lookup"><span data-stu-id="57be2-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="57be2-137">Si no se desea ningún objeto de datos de tabla, _lppTblData_ debe establecerse en NULL en lugar de un valor de puntero.</span><span class="sxs-lookup"><span data-stu-id="57be2-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="57be2-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57be2-138">Return value</span></span>

<span data-ttu-id="57be2-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="57be2-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57be2-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57be2-140">Remarks</span></span>

<span data-ttu-id="57be2-141">MAPI utiliza las funciones que señala _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación, en particular para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto Por ejemplo, [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="57be2-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="57be2-142">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="57be2-142">Notes to callers</span></span>

<span data-ttu-id="57be2-143">Todo lo posible leer desde el recurso de cuadro de diálogo, incluidos:</span><span class="sxs-lookup"><span data-stu-id="57be2-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="57be2-144">El título de la página que es, el miembro _ulbLpszLabel_ de la estructura [DTBLPAGE](dtblpage.md) leer desde el título del cuadro de diálogo en el recurso.</span><span class="sxs-lookup"><span data-stu-id="57be2-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="57be2-145">Todos los títulos de control que es, los miembros de _ulbLpszLabel_ de otras estructuras de control que se leen el texto del control en el recurso.</span><span class="sxs-lookup"><span data-stu-id="57be2-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="57be2-146">**BuildDisplayTable** sobrescribe cualquier cosa las estructuras de control de entrada con información pasada desde el recurso de cuadro de diálogo, lo que significa que el autor de la llamada de **BuildDisplayTable** no puede especificar dinámicamente los títulos de página o un control.</span><span class="sxs-lookup"><span data-stu-id="57be2-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="57be2-147">Los autores de llamadas que necesitan para hacer que pueden tener **BuildDisplayTable** devuelven el objeto de datos de tabla en _lppTableData_ y cambian filas en ella; o bien, puede crear en su lugar en la tabla para mostrar manualmente en un objeto de datos de tabla.</span><span class="sxs-lookup"><span data-stu-id="57be2-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="57be2-148">Si _lppTableData_ no está establecido en NULL, el proveedor es responsable de liberar el objeto de datos de la tabla cuando haya terminado con la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="57be2-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

