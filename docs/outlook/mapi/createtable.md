---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435015"
---
# <a name="createtable"></a><span data-ttu-id="a3349-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="a3349-103">CreateTable</span></span>

  
  
<span data-ttu-id="a3349-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3349-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3349-105">Crea estructuras y un identificador de objeto para un [objeto ITableData](itabledataiunknown.md) que se puede usar para crear contenido de tabla.</span><span class="sxs-lookup"><span data-stu-id="a3349-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3349-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a3349-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3349-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a3349-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a3349-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a3349-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3349-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a3349-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a3349-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a3349-110">Called by:</span></span>  <br/> |<span data-ttu-id="a3349-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a3349-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a><span data-ttu-id="a3349-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a3349-112">Parameters</span></span>

 <span data-ttu-id="a3349-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a3349-113">_lpInterface_</span></span>
  
> <span data-ttu-id="a3349-114">[in] Puntero a un identificador de interfaz (IID) para el objeto de datos de tabla.</span><span class="sxs-lookup"><span data-stu-id="a3349-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="a3349-115">El identificador de interfaz válido es IID_IMAPITableData.</span><span class="sxs-lookup"><span data-stu-id="a3349-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="a3349-116">Si se pasa NULL en el parámetro  _lpInterface,_ también se convierte el objeto de datos de tabla devuelto en el parámetro  _lppTableData_ en la interfaz estándar de un objeto de datos de tabla.</span><span class="sxs-lookup"><span data-stu-id="a3349-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="a3349-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="a3349-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="a3349-118">[in] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="a3349-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="a3349-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="a3349-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="a3349-120">[in] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="a3349-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="a3349-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="a3349-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="a3349-122">[in] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="a3349-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="a3349-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="a3349-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="a3349-124">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a3349-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="a3349-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="a3349-125">_ulTableType_</span></span>
  
> <span data-ttu-id="a3349-126">[in] Un tipo de tabla que está disponible para una aplicación cliente o un proveedor de servicios como parte de [imapitable::GetStatus](imapitable-getstatus.md) devuelven datos en sus vistas de tabla.</span><span class="sxs-lookup"><span data-stu-id="a3349-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="a3349-127">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="a3349-127">Possible values are:</span></span> 
    
<span data-ttu-id="a3349-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="a3349-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="a3349-129">El contenido de la tabla es dinámico y puede cambiar a medida que cambian los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="a3349-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="a3349-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="a3349-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="a3349-131">Las filas de la tabla son fijas, pero los valores de estas filas son dinámicos y pueden cambiar a medida que cambian los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="a3349-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="a3349-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="a3349-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="a3349-133">La tabla es estática y el contenido no cambia cuando cambian los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="a3349-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="a3349-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="a3349-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="a3349-135">[in] Número de índice de la columna para su uso al cambiar los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a3349-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="a3349-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="a3349-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="a3349-137">[in] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indica las propiedades necesarias en la tabla para la que el objeto contiene datos.</span><span class="sxs-lookup"><span data-stu-id="a3349-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="a3349-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="a3349-138">_lppTableData_</span></span>
  
> <span data-ttu-id="a3349-139">[salida] Puntero a un puntero al objeto de datos de tabla devuelto.</span><span class="sxs-lookup"><span data-stu-id="a3349-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3349-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3349-140">Return value</span></span>

<span data-ttu-id="a3349-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3349-141">S_OK</span></span> 
  
> <span data-ttu-id="a3349-142">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="a3349-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3349-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3349-143">Remarks</span></span>

<span data-ttu-id="a3349-144">Los parámetros de entrada  _lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ apuntan a las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer,](mapifreebuffer.md) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a3349-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="a3349-145">Una aplicación cliente que llama **a CreateTable** pasa punteros a las funciones MAPI que se han denominado; un proveedor de servicios pasa los punteros a estas funciones que recibió en su llamada de inicialización o recuperó con una llamada al método [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md)</span><span class="sxs-lookup"><span data-stu-id="a3349-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3349-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3349-146">See also</span></span>



[<span data-ttu-id="a3349-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3349-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

