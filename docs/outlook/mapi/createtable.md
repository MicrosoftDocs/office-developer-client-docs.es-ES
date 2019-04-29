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
# <a name="createtable"></a><span data-ttu-id="01f99-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="01f99-103">CreateTable</span></span>

  
  
<span data-ttu-id="01f99-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01f99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01f99-105">Crea estructuras y un identificador de objeto para un objeto [ITableData](itabledataiunknown.md) que se puede usar para crear el contenido de la tabla.</span><span class="sxs-lookup"><span data-stu-id="01f99-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f99-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="01f99-106">Header file:</span></span>  <br/> |<span data-ttu-id="01f99-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="01f99-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="01f99-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="01f99-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="01f99-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01f99-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01f99-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="01f99-110">Called by:</span></span>  <br/> |<span data-ttu-id="01f99-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="01f99-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="01f99-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="01f99-112">Parameters</span></span>

 <span data-ttu-id="01f99-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="01f99-113">_lpInterface_</span></span>
  
> <span data-ttu-id="01f99-114">a Puntero a un identificador de interfaz (IID) para el objeto de datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="01f99-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="01f99-115">El identificador de interfaz válido es IID_IMAPITableData.</span><span class="sxs-lookup"><span data-stu-id="01f99-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="01f99-116">Pasar NULL en el parámetro _lpInterface_ también hace que el objeto de datos de la tabla devuelto en el parámetro _lppTableData_ se convierta en la interfaz estándar de un objeto de datos de tabla.</span><span class="sxs-lookup"><span data-stu-id="01f99-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="01f99-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="01f99-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="01f99-118">a Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se va a usar para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="01f99-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="01f99-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="01f99-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="01f99-120">a Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se va a usar para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="01f99-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="01f99-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="01f99-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="01f99-122">a Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="01f99-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="01f99-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="01f99-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="01f99-124">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="01f99-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="01f99-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="01f99-125">_ulTableType_</span></span>
  
> <span data-ttu-id="01f99-126">a Un tipo de tabla que está disponible para una aplicación cliente o un proveedor de servicios como parte de los datos de devolución de [IMAPITable:: getStatus](imapitable-getstatus.md) en sus vistas de tabla.</span><span class="sxs-lookup"><span data-stu-id="01f99-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="01f99-127">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="01f99-127">Possible values are:</span></span> 
    
<span data-ttu-id="01f99-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="01f99-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="01f99-129">El contenido de la tabla es dinámico y puede cambiar cuando se modifican los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="01f99-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="01f99-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="01f99-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="01f99-131">Las filas de la tabla son fijas, pero los valores de estas filas son dinámicos y pueden cambiar cuando cambian los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="01f99-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="01f99-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="01f99-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="01f99-133">La tabla es estática y el contenido no cambia cuando cambian los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="01f99-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="01f99-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="01f99-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="01f99-135">a Número de índice de la columna que se va a usar al cambiar los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="01f99-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="01f99-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="01f99-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="01f99-137">a Puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indica las propiedades necesarias en la tabla para la que el objeto contiene datos.</span><span class="sxs-lookup"><span data-stu-id="01f99-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="01f99-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="01f99-138">_lppTableData_</span></span>
  
> <span data-ttu-id="01f99-139">contempla Puntero a un puntero al objeto de datos de la tabla devuelta.</span><span class="sxs-lookup"><span data-stu-id="01f99-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01f99-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01f99-140">Return value</span></span>

<span data-ttu-id="01f99-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="01f99-141">S_OK</span></span> 
  
> <span data-ttu-id="01f99-142">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="01f99-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01f99-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01f99-143">Remarks</span></span>

<span data-ttu-id="01f99-144">Los parámetros de entrada _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ apuntan a las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="01f99-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="01f99-145">Una aplicación cliente que llama a **createTable** pasa en punteros a las funciones de MAPI que acaban de denominar; un proveedor de servicios pasa los punteros a estas funciones que recibió en su llamada de inicialización o que se recuperaron con una llamada al método [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md)</span><span class="sxs-lookup"><span data-stu-id="01f99-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01f99-146">Ver también</span><span class="sxs-lookup"><span data-stu-id="01f99-146">See also</span></span>



[<span data-ttu-id="01f99-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="01f99-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

