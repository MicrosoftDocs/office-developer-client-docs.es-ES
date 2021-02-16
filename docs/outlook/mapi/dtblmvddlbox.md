---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420748"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="23a85-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="23a85-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="23a85-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23a85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23a85-105">Describe una lista desplegable que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="23a85-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23a85-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="23a85-106">Header file:</span></span>  <br/> |<span data-ttu-id="23a85-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23a85-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="23a85-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="23a85-108">Members</span></span>

 <span data-ttu-id="23a85-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="23a85-109">**ulFlags**</span></span>
  
> <span data-ttu-id="23a85-110">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="23a85-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="23a85-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="23a85-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="23a85-112">Etiqueta de propiedad para una propiedad multivalor de tipo PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="23a85-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="23a85-113">Los diferentes valores de esta propiedad se muestran como entradas distintas en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="23a85-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23a85-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23a85-114">Remarks</span></span>

<span data-ttu-id="23a85-115">Una **estructura DTBLMVDDLBOX** describe una lista desplegable de varios valores, una lista de elementos de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="23a85-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="23a85-116">Al usar una lista desplegable de varios valores, los valores se muestran cuando un usuario hace clic en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="23a85-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="23a85-117">Los datos que se muestran proceden de la propiedad identificada en el **miembro ulMVPropTag.**</span><span class="sxs-lookup"><span data-stu-id="23a85-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="23a85-118">No es necesario leer desde la interfaz de propiedades asociada a la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="23a85-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="23a85-119">Además, como los usuarios no pueden realizar selecciones de estos tipos de cuadros de lista, los datos no se escriben en la interfaz de propiedades.</span><span class="sxs-lookup"><span data-stu-id="23a85-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="23a85-120">Solo se admiten propiedades de cadena de varios valores para la lista desplegable de varios valores; no se admiten otros tipos de propiedades multivalor.</span><span class="sxs-lookup"><span data-stu-id="23a85-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="23a85-121">Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="23a85-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="23a85-122">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [Implementar una tabla para mostrar.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="23a85-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23a85-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="23a85-123">See also</span></span>



[<span data-ttu-id="23a85-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="23a85-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="23a85-125">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="23a85-125">MAPI Structures</span></span>](mapi-structures.md)

