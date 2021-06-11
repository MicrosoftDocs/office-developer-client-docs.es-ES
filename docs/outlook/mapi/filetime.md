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
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409506"
---
# <a name="filetime"></a><span data-ttu-id="3c2f9-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="3c2f9-103">FILETIME</span></span>

  
  
<span data-ttu-id="3c2f9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c2f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c2f9-105">Contiene un valor de fecha y hora de 64 bits sin signo para un archivo.</span><span class="sxs-lookup"><span data-stu-id="3c2f9-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="3c2f9-106">Este valor representa el número de unidades de 100 nanosegundos desde el inicio del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="3c2f9-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c2f9-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3c2f9-107">Header file:</span></span>  <br/> |<span data-ttu-id="3c2f9-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c2f9-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="3c2f9-109">Members</span><span class="sxs-lookup"><span data-stu-id="3c2f9-109">Members</span></span>

 <span data-ttu-id="3c2f9-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="3c2f9-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="3c2f9-111">Orden bajo 32 bits del valor de tiempo del archivo.</span><span class="sxs-lookup"><span data-stu-id="3c2f9-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="3c2f9-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="3c2f9-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="3c2f9-113">Orden alto 32 bits del valor de tiempo del archivo.</span><span class="sxs-lookup"><span data-stu-id="3c2f9-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3c2f9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c2f9-114">Remarks</span></span>

<span data-ttu-id="3c2f9-115">Una propiedad de tipo PT_SYSTIME tiene una **estructura FILETIME** para su valor.</span><span class="sxs-lookup"><span data-stu-id="3c2f9-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="3c2f9-116">Dicha propiedad tiene un tipo **de datos FILETIME** para el **miembro Value** en su definición en una [estructura SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="3c2f9-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="3c2f9-117">La definición de la **estructura FILETIME** se encuentra en la Referencia del programador de  _Win32_ y en el archivo de encabezado MAPI Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="3c2f9-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="3c2f9-118">MAPI define la estructura condicionalmente para asegurarse de que se define cuando la definición de Win32 no está disponible.</span><span class="sxs-lookup"><span data-stu-id="3c2f9-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c2f9-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c2f9-119">See also</span></span>



[<span data-ttu-id="3c2f9-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3c2f9-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3c2f9-121">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="3c2f9-121">MAPI Structures</span></span>](mapi-structures.md)

