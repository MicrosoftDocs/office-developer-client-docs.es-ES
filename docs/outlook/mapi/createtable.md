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
ms.openlocfilehash: 5d4717dad51e7e6b90da59d285268761eec84d7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564153"
---
# <a name="createtable"></a><span data-ttu-id="48596-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="48596-103">CreateTable</span></span>

  
  
<span data-ttu-id="48596-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48596-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48596-105">Crea estructuras y un identificador de objeto para un objeto [ITableData](itabledataiunknown.md) que puede usarse para crear contenido de la tabla.</span><span class="sxs-lookup"><span data-stu-id="48596-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48596-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="48596-106">Header file:</span></span>  <br/> |<span data-ttu-id="48596-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="48596-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="48596-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="48596-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="48596-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="48596-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="48596-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="48596-110">Called by:</span></span>  <br/> |<span data-ttu-id="48596-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="48596-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="48596-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48596-112">Parameters</span></span>

 <span data-ttu-id="48596-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="48596-113">_lpInterface_</span></span>
  
> <span data-ttu-id="48596-114">[entrada] Puntero a un identificador de interfaz (IID) para el objeto de datos de tabla.</span><span class="sxs-lookup"><span data-stu-id="48596-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="48596-115">El identificador de interfaz válido es IID_IMAPITableData.</span><span class="sxs-lookup"><span data-stu-id="48596-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="48596-116">También pasando NULL en el parámetro _lpInterface_ hace que el objeto de datos de tabla devuelto en el parámetro _lppTableData_ a convertirse a la interfaz estándar para un objeto de datos de tabla.</span><span class="sxs-lookup"><span data-stu-id="48596-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="48596-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="48596-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="48596-118">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="48596-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="48596-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="48596-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="48596-120">[entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="48596-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="48596-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="48596-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="48596-122">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="48596-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="48596-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="48596-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="48596-124">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="48596-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="48596-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="48596-125">_ulTableType_</span></span>
  
> <span data-ttu-id="48596-126">[entrada] Un tipo de tabla que está disponible para una aplicación de cliente o un proveedor de servicios como parte de los datos devueltos de [IMAPITable::GetStatus](imapitable-getstatus.md) en sus vistas de tabla.</span><span class="sxs-lookup"><span data-stu-id="48596-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="48596-127">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="48596-127">Possible values are:</span></span> 
    
<span data-ttu-id="48596-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="48596-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="48596-129">Contenido de la tabla es dinámico y puede cambiar como los cambios de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="48596-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="48596-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="48596-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="48596-131">Se corrigen las filas de la tabla, pero los valores en estas filas son dinámicos y pueden cambiar como los cambios de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="48596-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="48596-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="48596-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="48596-133">En la tabla es estática, y el contenido no cambia cuando cambian los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="48596-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="48596-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="48596-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="48596-135">[entrada] Número de índice de la columna para su uso al cambiar los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="48596-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="48596-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="48596-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="48596-137">[entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas (propiedad) que indica las propiedades necesarias en la tabla para la que el objeto contiene datos.</span><span class="sxs-lookup"><span data-stu-id="48596-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="48596-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="48596-138">_lppTableData_</span></span>
  
> <span data-ttu-id="48596-139">[out] Puntero a un puntero al objeto de datos de tabla devuelta.</span><span class="sxs-lookup"><span data-stu-id="48596-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="48596-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48596-140">Return value</span></span>

<span data-ttu-id="48596-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="48596-141">S_OK</span></span> 
  
> <span data-ttu-id="48596-142">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="48596-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48596-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48596-143">Remarks</span></span>

<span data-ttu-id="48596-144">Los parámetros de entrada _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ , seleccione la [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y funciones [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="48596-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="48596-145">Una aplicación de cliente al llamar a **CreateTable** pasa punteros a las funciones MAPI que se acaba de asignar nombre; un proveedor de servicios pasa los punteros a estas funciones que reciben en su llamada de inicialización o recuperado con una llamada al método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="48596-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48596-146">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="48596-146">See also</span></span>



[<span data-ttu-id="48596-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48596-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

