---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 92540159386e6f37d93684aff037b235071010f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817985"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="5d871-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="5d871-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="5d871-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d871-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d871-105">Recupera una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="5d871-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="5d871-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d871-106">Parameters</span></span>

 <span data-ttu-id="5d871-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="5d871-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="5d871-108">[entrada] Un puntero a una estructura de valor de propiedad que describe la columna de índice de la fila que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5d871-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="5d871-109">El miembro **ulPropTag** de la estructura del valor de propiedad debe contener la misma etiqueta de propiedad como el parámetro _ulPropTagIndexColumn_ de la llamada a la función [CreateTable](createtable.md) , que obtiene acceso a la implementación de [ITableData](itabledataiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="5d871-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="5d871-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="5d871-110">_lppSRow_</span></span>
  
> <span data-ttu-id="5d871-111">[out] Un puntero a un puntero a la fila recuperada.</span><span class="sxs-lookup"><span data-stu-id="5d871-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="5d871-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="5d871-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="5d871-113">[entrada, salida] En la entrada, un puntero válido o NULL, que indica que no hay información necesita que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="5d871-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="5d871-114">En la salida, un puntero válido que apunta al número de fila de la fila, un número secuencial que identifica la posición de la fila en la tabla.</span><span class="sxs-lookup"><span data-stu-id="5d871-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5d871-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d871-115">Return value</span></span>

<span data-ttu-id="5d871-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5d871-116">S_OK</span></span> 
  
> <span data-ttu-id="5d871-117">La fila se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5d871-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="5d871-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5d871-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="5d871-119">El [SPropValue](spropvalue.md) estructura que señala _lpSPropValue_ no contiene la propiedad de columna de índice.</span><span class="sxs-lookup"><span data-stu-id="5d871-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5d871-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d871-120">Remarks</span></span>

<span data-ttu-id="5d871-121">El método **ITableData::HrQueryRow** recupera todas las propiedades de la fila que tiene una columna de índice que coincide con el valor de la columna de índice incluido en la estructura de propiedad que señala _lpSPropValue_.</span><span class="sxs-lookup"><span data-stu-id="5d871-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="5d871-122">**HrQueryRow** también devuelve el número de fila, si el autor de la llamada lo solicita, que identifica la posición de la fila en la tabla.</span><span class="sxs-lookup"><span data-stu-id="5d871-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="5d871-123">Debido a que **HrQueryRow** no modifique la estructura de **SPropValue** que señala _lpSPropValue_, los autores de llamadas deben liberar la estructura cuando devuelve **HrQueryRow** .</span><span class="sxs-lookup"><span data-stu-id="5d871-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="5d871-124">Los autores de llamadas también deben liberar la estructura **SRow** que contiene la fila recuperada.</span><span class="sxs-lookup"><span data-stu-id="5d871-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d871-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d871-125">See also</span></span>



[<span data-ttu-id="5d871-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="5d871-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="5d871-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5d871-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5d871-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5d871-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="5d871-129">SRow</span><span class="sxs-lookup"><span data-stu-id="5d871-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="5d871-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d871-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

