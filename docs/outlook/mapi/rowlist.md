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
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820541"
---
# <a name="rowlist"></a><span data-ttu-id="057b1-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="057b1-103">ROWLIST</span></span>

  
  
<span data-ttu-id="057b1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="057b1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="057b1-105">Contiene una matriz de estructuras [ROWENTRY](rowentry.md) que representa las filas y las operaciones que se realizan en las filas de una tabla a través de la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="057b1-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="057b1-106">Members</span><span class="sxs-lookup"><span data-stu-id="057b1-106">Members</span></span>

 <span data-ttu-id="057b1-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="057b1-107">**cEntries**</span></span>
  
> <span data-ttu-id="057b1-108">Número de entradas en la matriz especificada por el miembro **aEntries** .</span><span class="sxs-lookup"><span data-stu-id="057b1-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="057b1-109">**aEntries [MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="057b1-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="057b1-110">Matriz de estructuras **ROWENTRY** que contiene las filas y las operaciones que se realizan en las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="057b1-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="057b1-111">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="057b1-111">MFCMAPI reference</span></span>

<span data-ttu-id="057b1-112">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="057b1-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="057b1-113">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="057b1-113">**File**</span></span>|<span data-ttu-id="057b1-114">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="057b1-114">**Function**</span></span>|<span data-ttu-id="057b1-115">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="057b1-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="057b1-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="057b1-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="057b1-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="057b1-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="057b1-118">Se usa para crear una lista de reglas seleccionadas para **ModifyTable** las acciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="057b1-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="057b1-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="057b1-119">See also</span></span>



[<span data-ttu-id="057b1-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="057b1-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="057b1-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="057b1-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="057b1-122">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="057b1-122">MAPI Structures</span></span>](mapi-structures.md)

