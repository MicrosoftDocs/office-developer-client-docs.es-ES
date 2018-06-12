---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: f8ac73b1977886208290285fec2d1bd0de1b4f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820543"
---
# <a name="rowentry"></a><span data-ttu-id="b627b-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="b627b-103">ROWENTRY</span></span>

<span data-ttu-id="b627b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b627b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b627b-105">Contiene una fila y la operación que se lleva a cabo en esa fila en una tabla a través de la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="b627b-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="b627b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b627b-106">Members</span></span>

<span data-ttu-id="b627b-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="b627b-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="b627b-108">Una de las siguientes operaciones se realicen en los datos:</span><span class="sxs-lookup"><span data-stu-id="b627b-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="b627b-109">ROW_ADD: Agregar los datos a la tabla como una nueva fila.</span><span class="sxs-lookup"><span data-stu-id="b627b-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="b627b-110">ROW_MODIFY: Modificar esta fila en la tabla.</span><span class="sxs-lookup"><span data-stu-id="b627b-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="b627b-111">ROW_REMOVE: Quitar esta fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b627b-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="b627b-112">ROW_EMPTY: No agregue la fila de datos a la tabla.</span><span class="sxs-lookup"><span data-stu-id="b627b-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="b627b-113">(La fila está vacía).</span><span class="sxs-lookup"><span data-stu-id="b627b-113">(The row is empty.)</span></span>
    
<span data-ttu-id="b627b-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b627b-114">**cValues**</span></span>
  
> <span data-ttu-id="b627b-115">El número de valores de propiedad en **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="b627b-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="b627b-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="b627b-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="b627b-117">Una matriz de estructuras [SPropValue](spropvalue.md) que representa los valores de las columnas que se insertará en la tabla.</span><span class="sxs-lookup"><span data-stu-id="b627b-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="b627b-118">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b627b-118">MFCMAPI reference</span></span>

<span data-ttu-id="b627b-119">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b627b-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b627b-120">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b627b-120">**File**</span></span>|<span data-ttu-id="b627b-121">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="b627b-121">**Function**</span></span>|<span data-ttu-id="b627b-122">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b627b-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b627b-123">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b627b-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="b627b-124">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="b627b-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="b627b-125">Se usa para crear una lista de reglas seleccionadas para **ModifyTable** las acciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b627b-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b627b-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="b627b-126">See also</span></span>
  
- [<span data-ttu-id="b627b-127">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b627b-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="b627b-128">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="b627b-128">MAPI Structures</span></span>](mapi-structures.md)

