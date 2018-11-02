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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fb0bfaba1ca0a0d7d34096b3b0b1db9863207097
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576270"
---
# <a name="rowentry"></a><span data-ttu-id="ed161-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="ed161-103">ROWENTRY</span></span>

<span data-ttu-id="ed161-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed161-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed161-105">Contiene una fila y la operación que se lleva a cabo en esa fila en una tabla a través de la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ed161-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="ed161-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ed161-106">Members</span></span>

<span data-ttu-id="ed161-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="ed161-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="ed161-108">Una de las siguientes operaciones se realicen en los datos:</span><span class="sxs-lookup"><span data-stu-id="ed161-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="ed161-109">ROW_ADD: Agregar los datos a la tabla como una nueva fila.</span><span class="sxs-lookup"><span data-stu-id="ed161-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="ed161-110">ROW_MODIFY: Modificar esta fila en la tabla.</span><span class="sxs-lookup"><span data-stu-id="ed161-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="ed161-111">ROW_REMOVE: Quitar esta fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ed161-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="ed161-112">ROW_EMPTY: No agregue la fila de datos a la tabla.</span><span class="sxs-lookup"><span data-stu-id="ed161-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="ed161-113">(La fila está vacía).</span><span class="sxs-lookup"><span data-stu-id="ed161-113">(The row is empty.)</span></span>
    
<span data-ttu-id="ed161-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="ed161-114">**cValues**</span></span>
  
> <span data-ttu-id="ed161-115">El número de valores de propiedad en **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="ed161-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="ed161-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="ed161-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="ed161-117">Una matriz de estructuras [SPropValue](spropvalue.md) que representa los valores de las columnas que se insertará en la tabla.</span><span class="sxs-lookup"><span data-stu-id="ed161-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ed161-118">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ed161-118">MFCMAPI reference</span></span>

<span data-ttu-id="ed161-119">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ed161-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ed161-120">**File**</span><span class="sxs-lookup"><span data-stu-id="ed161-120">**File**</span></span>|<span data-ttu-id="ed161-121">**Función**</span><span class="sxs-lookup"><span data-stu-id="ed161-121">**Function**</span></span>|<span data-ttu-id="ed161-122">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ed161-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ed161-123">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ed161-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="ed161-124">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="ed161-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="ed161-125">Se usa para crear una lista de reglas seleccionadas para **ModifyTable** las acciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ed161-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed161-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed161-126">See also</span></span>
  
- [<span data-ttu-id="ed161-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed161-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="ed161-128">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="ed161-128">MAPI Structures</span></span>](mapi-structures.md)

