---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418375"
---
# <a name="itabledatahrenumrow"></a><span data-ttu-id="bc06a-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="bc06a-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="bc06a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc06a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc06a-105">Recupera una fila en función de su posición en la tabla.</span><span class="sxs-lookup"><span data-stu-id="bc06a-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="bc06a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="bc06a-106">Parameters</span></span>

 <span data-ttu-id="bc06a-107">_ulRowNumber_</span><span class="sxs-lookup"><span data-stu-id="bc06a-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="bc06a-108">[in] Número de fila para la que se devuelven las propiedades.</span><span class="sxs-lookup"><span data-stu-id="bc06a-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="bc06a-109">El valor del parámetro  _ulRowNumber_ puede ser cualquier valor desde 0, que indica la primera fila de la tabla, a través de n - 1, que indica la última fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="bc06a-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="bc06a-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="bc06a-110">_lppSRow_</span></span>
  
> <span data-ttu-id="bc06a-111">[salida] Puntero a un puntero a una [estructura SRow](srow.md) que describe la fila de destino.</span><span class="sxs-lookup"><span data-stu-id="bc06a-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bc06a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc06a-112">Return value</span></span>

<span data-ttu-id="bc06a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc06a-113">S_OK</span></span> 
  
> <span data-ttu-id="bc06a-114">La fila se recuperó correctamente o no existe una fila para el número de fila especificado por el _parámetro ulRowNumber._</span><span class="sxs-lookup"><span data-stu-id="bc06a-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bc06a-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc06a-115">Remarks</span></span>

<span data-ttu-id="bc06a-116">El **método ITableData::HrEnumRow** recupera una fila basada en un número secuencial.</span><span class="sxs-lookup"><span data-stu-id="bc06a-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="bc06a-117">Este número representa el orden de inserción (0 indica la primera fila y el número de filas menos 1 indica la última fila).</span><span class="sxs-lookup"><span data-stu-id="bc06a-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="bc06a-118">MAPI mantiene este orden cronológico de inserción de filas durante la duración del objeto de datos de tabla.</span><span class="sxs-lookup"><span data-stu-id="bc06a-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="bc06a-119">Si el número especificado en  _ulRowNumber_ no corresponde a una fila de la tabla, **HrEnumRow** devuelve S_OK y establece el parámetro  _lppSRow_ en NULL.</span><span class="sxs-lookup"><span data-stu-id="bc06a-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="bc06a-120">MAPI asigna memoria para la estructura **SRow** devuelta mediante la [función MAPIAllocateBuffer](mapiallocatebuffer.md) cuando se crea el objeto de datos de tabla.</span><span class="sxs-lookup"><span data-stu-id="bc06a-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="bc06a-121">El autor de la llamada debe liberar esta memoria llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="bc06a-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="bc06a-122">Para recuperar filas de una tabla en el orden en que se insertaron, los usuarios del objeto de datos de tabla llaman al **método HrEnumRow.**</span><span class="sxs-lookup"><span data-stu-id="bc06a-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc06a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc06a-123">See also</span></span>



[<span data-ttu-id="bc06a-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="bc06a-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="bc06a-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bc06a-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bc06a-126">SRow</span><span class="sxs-lookup"><span data-stu-id="bc06a-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="bc06a-127">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc06a-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

