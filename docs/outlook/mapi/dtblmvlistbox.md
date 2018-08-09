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
ms.openlocfilehash: 0de5bf5d5bb4d8c5606e97bdbc6e70493609a05f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816742"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="db391-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="db391-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="db391-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db391-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="db391-105">Describe una lista de varios valores que se mostrará en un cuadro de diálogo que se genera a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="db391-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db391-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="db391-106">Header file:</span></span>  <br/> |<span data-ttu-id="db391-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db391-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="db391-108">Members</span><span class="sxs-lookup"><span data-stu-id="db391-108">Members</span></span>

 <span data-ttu-id="db391-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="db391-109">**ulFlags**</span></span>
  
> <span data-ttu-id="db391-110">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="db391-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="db391-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="db391-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="db391-112">Etiqueta de propiedad de una propiedad con varios valores de tipo PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="db391-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="db391-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db391-113">Remarks</span></span>

<span data-ttu-id="db391-114">Una estructura **DTBLMVLISTBOX** describe una lista de varios valores estándar que tiene una lista de solo lectura de elementos.</span><span class="sxs-lookup"><span data-stu-id="db391-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="db391-115">Mediante el uso de una lista de varios valores estándar, los valores se muestran inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="db391-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="db391-116">Los datos que se muestran proceden de la propiedad identificada en el miembro **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="db391-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="db391-117">No hay ningún requisito para leer desde la interfaz de propiedad que está asociada a la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="db391-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="db391-118">Además, debido a que los usuarios no son puedan realizar selecciones de estos tipos de listas, datos no se escriben en la interfaz (propiedad).</span><span class="sxs-lookup"><span data-stu-id="db391-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="db391-119">Propiedades de cadena multivalor sólo son compatibles con la lista de varios valores; otros tipos de propiedad de varios valores no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="db391-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="db391-120">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="db391-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="db391-121">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="db391-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db391-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="db391-122">See also</span></span>



[<span data-ttu-id="db391-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="db391-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="db391-124">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="db391-124">MAPI Structures</span></span>](mapi-structures.md)

