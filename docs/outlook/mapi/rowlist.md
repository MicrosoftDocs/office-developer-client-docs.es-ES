---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419187"
---
# <a name="rowlist"></a><span data-ttu-id="1bfeb-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="1bfeb-103">ROWLIST</span></span>

  
  
<span data-ttu-id="1bfeb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bfeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bfeb-105">Contiene una matriz de estructuras [ROWENTRY](rowentry.md) que representan filas y las operaciones que se realizan en esas filas de una tabla a través de la [interfaz IExchangeModifyTable.](iexchangemodifytableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="1bfeb-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="1bfeb-106">Members</span><span class="sxs-lookup"><span data-stu-id="1bfeb-106">Members</span></span>

 <span data-ttu-id="1bfeb-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="1bfeb-107">**cEntries**</span></span>
  
> <span data-ttu-id="1bfeb-108">Recuento de entradas en la matriz especificada por el **miembro aEntries.**</span><span class="sxs-lookup"><span data-stu-id="1bfeb-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="1bfeb-109">**aEntries[MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="1bfeb-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="1bfeb-110">Matriz de **estructuras ROWENTRY** que contiene las filas y las operaciones que se realizan en esas filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="1bfeb-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="1bfeb-111">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1bfeb-111">MFCMAPI reference</span></span>

<span data-ttu-id="1bfeb-112">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1bfeb-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1bfeb-113">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1bfeb-113">**File**</span></span>|<span data-ttu-id="1bfeb-114">**Función**</span><span class="sxs-lookup"><span data-stu-id="1bfeb-114">**Function**</span></span>|<span data-ttu-id="1bfeb-115">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1bfeb-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1bfeb-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1bfeb-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="1bfeb-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="1bfeb-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="1bfeb-118">Se usa para crear una lista de reglas seleccionadas para acciones **de ModifyTable posteriores.**</span><span class="sxs-lookup"><span data-stu-id="1bfeb-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1bfeb-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bfeb-119">See also</span></span>



[<span data-ttu-id="1bfeb-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="1bfeb-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="1bfeb-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1bfeb-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="1bfeb-122">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="1bfeb-122">MAPI Structures</span></span>](mapi-structures.md)

