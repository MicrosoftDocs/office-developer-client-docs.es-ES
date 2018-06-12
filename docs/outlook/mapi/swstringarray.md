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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820815"
---
# <a name="swstringarray"></a><span data-ttu-id="9adcd-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="9adcd-103">SWStringArray</span></span>

  
  
<span data-ttu-id="9adcd-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9adcd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9adcd-105">Contiene una matriz de cadenas de caracteres que se utilizan para describir una propiedad de tipo PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="9adcd-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9adcd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9adcd-106">Header file:</span></span>  <br/> |<span data-ttu-id="9adcd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9adcd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="9adcd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9adcd-108">Members</span></span>

 <span data-ttu-id="9adcd-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="9adcd-109">**cValues**</span></span>
  
> <span data-ttu-id="9adcd-110">Recuento de las cadenas en la matriz indicada por el miembro **lppszW** .</span><span class="sxs-lookup"><span data-stu-id="9adcd-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="9adcd-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="9adcd-111">**lppszW**</span></span>
  
> <span data-ttu-id="9adcd-112">Puntero a una matriz de cadenas de caracteres Unicode terminado en null.</span><span class="sxs-lookup"><span data-stu-id="9adcd-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9adcd-113">Notas</span><span class="sxs-lookup"><span data-stu-id="9adcd-113">Remarks</span></span>

<span data-ttu-id="9adcd-114">Para obtener más información sobre PT_MV_UNICODE, vea [Tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="9adcd-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9adcd-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="9adcd-115">See also</span></span>



[<span data-ttu-id="9adcd-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9adcd-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="9adcd-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="9adcd-117">MAPI Structures</span></span>](mapi-structures.md)

