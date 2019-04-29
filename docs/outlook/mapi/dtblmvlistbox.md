---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439705"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="edc25-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="edc25-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="edc25-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edc25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edc25-105">Describe una lista con varios valores que se mostrará en un cuadro de diálogo que se genera a partir de una tabla de presentación.</span><span class="sxs-lookup"><span data-stu-id="edc25-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edc25-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="edc25-106">Header file:</span></span>  <br/> |<span data-ttu-id="edc25-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="edc25-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="edc25-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="edc25-108">Members</span></span>

 <span data-ttu-id="edc25-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="edc25-109">**ulFlags**</span></span>
  
> <span data-ttu-id="edc25-110">Reserve debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="edc25-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="edc25-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="edc25-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="edc25-112">Etiqueta de propiedad de una propiedad de varios valores de tipo PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="edc25-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="edc25-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edc25-113">Remarks</span></span>

<span data-ttu-id="edc25-114">Una estructura **DTBLMVLISTBOX** describe una lista estándar con varios valores que tiene una lista de solo lectura de elementos.</span><span class="sxs-lookup"><span data-stu-id="edc25-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="edc25-115">Mediante el uso de una lista estándar de varios valores, los valores se muestran inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="edc25-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="edc25-116">Los datos que se muestran provienen de la propiedad identificada en el miembro **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="edc25-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="edc25-117">No es necesario leer de la interfaz de propiedades asociada a la tabla de visualización.</span><span class="sxs-lookup"><span data-stu-id="edc25-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="edc25-118">Además, dado que los usuarios no pueden realizar selecciones de estos tipos de listas, los datos no se escriben en la interfaz de propiedades.</span><span class="sxs-lookup"><span data-stu-id="edc25-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="edc25-119">Solo se admiten propiedades de cadena de varios valores para la lista de varios valores; no se admiten otros tipos de propiedades con varios valores.</span><span class="sxs-lookup"><span data-stu-id="edc25-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="edc25-120">Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="edc25-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="edc25-121">Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="edc25-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="edc25-122">Ver también</span><span class="sxs-lookup"><span data-stu-id="edc25-122">See also</span></span>



[<span data-ttu-id="edc25-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="edc25-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="edc25-124">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="edc25-124">MAPI Structures</span></span>](mapi-structures.md)

