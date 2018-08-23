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
ms.openlocfilehash: 910f779f3463ee5dccd052655a442ef24c2cce58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570684"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="43718-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="43718-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="43718-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43718-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43718-105">Describe una lista desplegable que se usará en un cuadro de diálogo que se genera a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="43718-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43718-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="43718-106">Header file:</span></span>  <br/> |<span data-ttu-id="43718-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43718-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="43718-108">Members</span><span class="sxs-lookup"><span data-stu-id="43718-108">Members</span></span>

 <span data-ttu-id="43718-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="43718-109">**ulFlags**</span></span>
  
> <span data-ttu-id="43718-110">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="43718-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="43718-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="43718-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="43718-112">Etiqueta de propiedad de una propiedad con varios valores de tipo PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="43718-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="43718-113">Se muestran los distintos valores de esta propiedad como distintas entradas en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="43718-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43718-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43718-114">Remarks</span></span>

<span data-ttu-id="43718-115">Una estructura **DTBLMVDDLBOX** describe una lista desplegable multivalor una lista de solo lectura de elementos.</span><span class="sxs-lookup"><span data-stu-id="43718-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="43718-116">Mediante el uso de una lista desplegable con múltiples valores, los valores se muestran cuando un usuario hace clic en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="43718-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="43718-117">Los datos que se muestran proceden de la propiedad identificada en el miembro **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="43718-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="43718-118">No hay ningún requisito para leer desde la interfaz de propiedad que está asociada a la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="43718-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="43718-119">Además, debido a que los usuarios no son puedan realizar selecciones de estos tipos de cuadros de lista, datos no se escriben en la interfaz (propiedad).</span><span class="sxs-lookup"><span data-stu-id="43718-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="43718-120">Propiedades de cadena multivalor sólo son compatibles con la lista desplegable multivalor; otros tipos de propiedad de varios valores no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="43718-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="43718-121">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="43718-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="43718-122">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="43718-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43718-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="43718-123">See also</span></span>



[<span data-ttu-id="43718-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="43718-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="43718-125">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="43718-125">MAPI Structures</span></span>](mapi-structures.md)

