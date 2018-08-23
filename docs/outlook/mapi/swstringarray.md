---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e3f53a894b7f7cdaa68e66530c7bd99bf49b9ed0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581359"
---
# <a name="swstringarray"></a><span data-ttu-id="d2c49-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="d2c49-103">SWStringArray</span></span>

  
  
<span data-ttu-id="d2c49-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2c49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2c49-105">Contiene una matriz de cadenas de caracteres que se utilizan para describir una propiedad de tipo PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d2c49-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2c49-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d2c49-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2c49-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2c49-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="d2c49-108">Members</span><span class="sxs-lookup"><span data-stu-id="d2c49-108">Members</span></span>

 <span data-ttu-id="d2c49-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d2c49-109">**cValues**</span></span>
  
> <span data-ttu-id="d2c49-110">Recuento de las cadenas en la matriz indicada por el miembro **lppszW** .</span><span class="sxs-lookup"><span data-stu-id="d2c49-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="d2c49-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="d2c49-111">**lppszW**</span></span>
  
> <span data-ttu-id="d2c49-112">Puntero a una matriz de cadenas de caracteres Unicode terminado en null.</span><span class="sxs-lookup"><span data-stu-id="d2c49-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2c49-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2c49-113">Remarks</span></span>

<span data-ttu-id="d2c49-114">Para obtener más información sobre PT_MV_UNICODE, vea [Tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="d2c49-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2c49-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d2c49-115">See also</span></span>



[<span data-ttu-id="d2c49-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d2c49-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d2c49-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d2c49-117">MAPI Structures</span></span>](mapi-structures.md)

