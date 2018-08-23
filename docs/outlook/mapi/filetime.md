---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d58a216a41ff8fe93387ce6d9d1d6aa16f36f224
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583256"
---
# <a name="filetime"></a><span data-ttu-id="e14e3-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="e14e3-103">FILETIME</span></span>

  
  
<span data-ttu-id="e14e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e14e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e14e3-105">Contiene una fecha de 64 bits sin signo y el valor de tiempo de un archivo.</span><span class="sxs-lookup"><span data-stu-id="e14e3-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="e14e3-106">Este valor representa el número de unidades de 100 nanosegundos desde el inicio del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="e14e3-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e14e3-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e14e3-107">Header file:</span></span>  <br/> |<span data-ttu-id="e14e3-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e14e3-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="e14e3-109">Members</span><span class="sxs-lookup"><span data-stu-id="e14e3-109">Members</span></span>

 <span data-ttu-id="e14e3-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="e14e3-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="e14e3-111">Valor de tiempo de 32 bits de orden inferior del archivo.</span><span class="sxs-lookup"><span data-stu-id="e14e3-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="e14e3-112">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="e14e3-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="e14e3-113">Valor de tiempo de 32 bits de orden superior del archivo.</span><span class="sxs-lookup"><span data-stu-id="e14e3-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e14e3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e14e3-114">Remarks</span></span>

<span data-ttu-id="e14e3-115">Una propiedad de tipo PT_SYSTIME tiene una estructura **FILETIME** para su valor.</span><span class="sxs-lookup"><span data-stu-id="e14e3-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="e14e3-116">Este tipo de propiedad tiene un tipo de datos **FILETIME** para el miembro de **valor** en su definición en una estructura [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="e14e3-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="e14e3-117">La definición de la estructura **FILETIME** es en la _referencia del programador de Win32_ y en el archivo de encabezado Mapidefs.h MAPI.</span><span class="sxs-lookup"><span data-stu-id="e14e3-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="e14e3-118">MAPI define la estructura de forma condicional para asegurarse de que se define cuando no está disponible la definición de Win32.</span><span class="sxs-lookup"><span data-stu-id="e14e3-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e14e3-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e14e3-119">See also</span></span>



[<span data-ttu-id="e14e3-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e14e3-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e14e3-121">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="e14e3-121">MAPI Structures</span></span>](mapi-structures.md)

