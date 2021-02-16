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
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431599"
---
# <a name="builddisplaytable"></a><span data-ttu-id="a4eb8-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="a4eb8-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="a4eb8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4eb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4eb8-105">Crea una tabla para mostrar a partir de los datos de la página de propiedades contenidos en una o varias [estructuras DTPAGE.](dtpage.md)</span><span class="sxs-lookup"><span data-stu-id="a4eb8-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4eb8-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a4eb8-106">Header file:</span></span>  <br/> |<span data-ttu-id="a4eb8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a4eb8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a4eb8-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a4eb8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a4eb8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a4eb8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a4eb8-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a4eb8-110">Called by:</span></span>  <br/> |<span data-ttu-id="a4eb8-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a4eb8-111">Service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a4eb8-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4eb8-112">Parameters</span></span>

 <span data-ttu-id="a4eb8-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="a4eb8-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="a4eb8-114">[entrada] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="a4eb8-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="a4eb8-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="a4eb8-116">[entrada] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="a4eb8-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="a4eb8-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="a4eb8-118">[entrada] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="a4eb8-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="a4eb8-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="a4eb8-120">Sin usar; debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="a4eb8-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="a4eb8-121">_hInstance_</span></span>
  
> <span data-ttu-id="a4eb8-122">[entrada] Instancia de un objeto MAPI desde el que **BuildDisplayTable** recupera recursos.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="a4eb8-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="a4eb8-123">_cPages_</span></span>
  
> <span data-ttu-id="a4eb8-124">[entrada] Recuento de [estructuras DTPAGE](dtpage.md) en la matriz a la que apunta el _parámetro lpPage._</span><span class="sxs-lookup"><span data-stu-id="a4eb8-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="a4eb8-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="a4eb8-125">_lpPage_</span></span>
  
> <span data-ttu-id="a4eb8-126">[entrada] Puntero a una matriz **de estructuras DTPAGE** que contienen información sobre las páginas de tabla para mostrar que se crearán.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="a4eb8-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4eb8-127">_ulFlags_</span></span>
  
> <span data-ttu-id="a4eb8-128">[entrada] Máscara de bits de marcas.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="a4eb8-129">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="a4eb8-129">The following flag can be set:</span></span>
    
<span data-ttu-id="a4eb8-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a4eb8-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a4eb8-131">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a4eb8-132">Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="a4eb8-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="a4eb8-133">_lppTable_</span></span>
  
> <span data-ttu-id="a4eb8-134">[salida] Puntero a un puntero a la tabla para mostrar, que expone la [interfaz IMAPITable.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="a4eb8-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="a4eb8-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="a4eb8-135">_lppTblData_</span></span>
  
> <span data-ttu-id="a4eb8-136">[entrada, salida] Puntero a un puntero a un objeto de datos de tabla que expone la [interfaz ITableData](itabledataiunknown.md) en la tabla devuelta en el _parámetro lppTable._</span><span class="sxs-lookup"><span data-stu-id="a4eb8-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="a4eb8-137">Si no se desea ningún objeto de datos de tabla,  _lppTblData_ debe establecerse en NULL en lugar de un valor de puntero.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a4eb8-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4eb8-138">Return value</span></span>

<span data-ttu-id="a4eb8-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a4eb8-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4eb8-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4eb8-140">Remarks</span></span>

<span data-ttu-id="a4eb8-141">MAPI usa las funciones a las que  _apuntan lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria, en particular para asignar memoria para que la usen las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="a4eb8-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a4eb8-142">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a4eb8-142">Notes to callers</span></span>

<span data-ttu-id="a4eb8-143">Todo lo posible se lee en el recurso de cuadro de diálogo, incluidos:</span><span class="sxs-lookup"><span data-stu-id="a4eb8-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="a4eb8-144">Título de página que es el  _miembro ulbLpszLabel_ de la estructura [DTBLPAGE](dtblpage.md) leído en el título del cuadro de diálogo en el recurso.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="a4eb8-145">Todos los títulos de control, es decir, los  _miembros ulbLpszLabel_ de otras estructuras de control leídos del texto del control en el recurso.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="a4eb8-146">**BuildDisplayTable** sobrescribe todo lo que se pasa en las estructuras de control de entrada con información del recurso de cuadro de diálogo, lo que significa que el llamador de **BuildDisplayTable** no puede especificar dinámicamente títulos de página o control.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="a4eb8-147">Los autores de llamadas que necesitan hacerlo pueden hacer **que BuildDisplayTable** devuelva el objeto de datos de tabla  _en lppTableData_ y cambie las filas en él; o bien, pueden crear la tabla para mostrar a mano en un objeto de datos de tabla en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="a4eb8-148">Si  _lppTableData_ no se establece en NULL, el proveedor es responsable de liberar el objeto de datos de tabla cuando termine con la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="a4eb8-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

