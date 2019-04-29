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
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436037"
---
# <a name="rowentry"></a><span data-ttu-id="0ca41-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="0ca41-103">ROWENTRY</span></span>

<span data-ttu-id="0ca41-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ca41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ca41-105">Contiene una fila y la operación que se realiza en esa fila en una tabla a través de la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="0ca41-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="0ca41-106">Members</span><span class="sxs-lookup"><span data-stu-id="0ca41-106">Members</span></span>

<span data-ttu-id="0ca41-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="0ca41-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="0ca41-108">Una de las siguientes operaciones que se realizarán en los datos:</span><span class="sxs-lookup"><span data-stu-id="0ca41-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="0ca41-109">ROW_ADD: Agregue los datos a la tabla como una fila nueva.</span><span class="sxs-lookup"><span data-stu-id="0ca41-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="0ca41-110">ROW_MODIFY: modifique esta fila en la tabla.</span><span class="sxs-lookup"><span data-stu-id="0ca41-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="0ca41-111">ROW_REMOVE: quitar esta fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0ca41-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="0ca41-112">ROW_EMPTY: no agregue los datos de fila a la tabla.</span><span class="sxs-lookup"><span data-stu-id="0ca41-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="0ca41-113">(La fila está vacía).</span><span class="sxs-lookup"><span data-stu-id="0ca41-113">(The row is empty.)</span></span>
    
<span data-ttu-id="0ca41-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0ca41-114">**cValues**</span></span>
  
> <span data-ttu-id="0ca41-115">Número de valores de propiedad en **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="0ca41-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="0ca41-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="0ca41-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="0ca41-117">Matriz de estructuras [SPropValue](spropvalue.md) que representa los valores de las columnas que se van a insertar en la tabla.</span><span class="sxs-lookup"><span data-stu-id="0ca41-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="0ca41-118">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0ca41-118">MFCMAPI reference</span></span>

<span data-ttu-id="0ca41-119">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="0ca41-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0ca41-120">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="0ca41-120">**File**</span></span>|<span data-ttu-id="0ca41-121">**Función**</span><span class="sxs-lookup"><span data-stu-id="0ca41-121">**Function**</span></span>|<span data-ttu-id="0ca41-122">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="0ca41-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0ca41-123">RulesDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="0ca41-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="0ca41-124">CRulesDlg:: GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="0ca41-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="0ca41-125">Se usa para crear una lista de reglas seleccionadas para las siguientes acciones **ModifyTable** .</span><span class="sxs-lookup"><span data-stu-id="0ca41-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ca41-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="0ca41-126">See also</span></span>
  
- [<span data-ttu-id="0ca41-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ca41-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="0ca41-128">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="0ca41-128">MAPI Structures</span></span>](mapi-structures.md)

