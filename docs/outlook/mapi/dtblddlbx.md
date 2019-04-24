---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340106"
---
# <a name="dtblddlbx"></a><span data-ttu-id="29fa7-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="29fa7-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="29fa7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29fa7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29fa7-105">Describe un control de lista desplegable que se utilizará en un cuadro de diálogo generado a partir de una tabla de presentación.</span><span class="sxs-lookup"><span data-stu-id="29fa7-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29fa7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="29fa7-106">Header file:</span></span>  <br/> |<span data-ttu-id="29fa7-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="29fa7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="29fa7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="29fa7-108">Members</span></span>

 <span data-ttu-id="29fa7-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="29fa7-109">**ulFlags**</span></span>
  
> <span data-ttu-id="29fa7-110">Reserved, debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="29fa7-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="29fa7-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="29fa7-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="29fa7-112">Etiqueta de propiedad de una propiedad de tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="29fa7-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="29fa7-113">Esta propiedad es una de las columnas de la tabla identificada por el miembro **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="29fa7-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="29fa7-114">Los valores de esta propiedad se muestran en la lista.</span><span class="sxs-lookup"><span data-stu-id="29fa7-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="29fa7-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="29fa7-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="29fa7-116">Etiqueta de propiedad de una propiedad de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="29fa7-116">Property tag for a property of any type.</span></span> <span data-ttu-id="29fa7-117">Esta propiedad es una de las columnas de la tabla identificada por el miembro **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="29fa7-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="29fa7-118">Cuando el usuario de la lista selecciona un valor de propiedad para el miembro **ulPRDisplayProperty** desde las filas de la tabla identificadas por el miembro **ulPRTableName** , se establece el miembro **ulPRSetProperty** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="29fa7-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="29fa7-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="29fa7-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="29fa7-120">Etiqueta de propiedad de una propiedad Table de tipo PT Object que se puede abrir mediante una llamada **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="29fa7-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="29fa7-121">La tabla debe tener dos columnas: **ulPRDisplayProperty** y **ulPRSetProperty**.</span><span class="sxs-lookup"><span data-stu-id="29fa7-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="29fa7-122">Las filas de la tabla deben coincidir con los elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="29fa7-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="29fa7-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29fa7-123">Remarks</span></span>

<span data-ttu-id="29fa7-124">Una estructura **DTBLDDLBX** describe un control de lista desplegable que se muestra como un elemento único hasta que el usuario elige expandirlo.</span><span class="sxs-lookup"><span data-stu-id="29fa7-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="29fa7-125">Las tres propiedades identificadas por las etiquetas de propiedad funcionan conjuntamente para mostrar la información de la lista y establecer una propiedad relacionada.</span><span class="sxs-lookup"><span data-stu-id="29fa7-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="29fa7-126">El miembro **ulPRTableName** es un objeto Table al que se tiene acceso a través de una llamada a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="29fa7-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="29fa7-127">La tabla tiene dos columnas: una columna para la propiedad identificada por el miembro **ulPRDisplayProperty** y otra para la propiedad identificada por el miembro **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="29fa7-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="29fa7-128">La propiedad **ulPRDisplayProperty** controla la presentación de la lista.</span><span class="sxs-lookup"><span data-stu-id="29fa7-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="29fa7-129">Cuando un usuario selecciona uno de los valores de la visualización, MAPI llama a [IMAPIProp:: SetProps](imapiprop-setprops.md) para establecer la propiedad correspondiente como identificada por el miembro **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="29fa7-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="29fa7-130">Esto significa que la propiedad de la misma fila que la propiedad de visualización seleccionada.</span><span class="sxs-lookup"><span data-stu-id="29fa7-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="29fa7-131">El miembro **ulPRSetProperty** no se puede establecer en **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="29fa7-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="29fa7-132">Se muestra un valor inicial en la lista si MAPI ha recuperado la propiedad representada por el miembro **ulPRSetProperty** mediante una llamada a [IMAPIProp:: GetProps](imapiprop-getprops.md) y ha ubicado una fila en la tabla con el valor para el miembro **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="29fa7-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="29fa7-133">El valor mostrado inicial es el contenido de la columna **ulPRDisplayProperty** de esa fila que coincide con la propiedad en el miembro **ulPRDisplayProperty** de la estructura.</span><span class="sxs-lookup"><span data-stu-id="29fa7-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="29fa7-134">El valor devuelto por **GetProps** para la propiedad identificada por el miembro **ulPRDisplayProperty** se convierte en el valor inicial que se muestra cuando se muestra la lista por primera vez.</span><span class="sxs-lookup"><span data-stu-id="29fa7-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="29fa7-135">Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="29fa7-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="29fa7-136">Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="29fa7-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="29fa7-137">Para obtener información acerca de los tipos de propiedades, consulte [MAPI Property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="29fa7-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29fa7-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="29fa7-138">See also</span></span>



[<span data-ttu-id="29fa7-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="29fa7-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="29fa7-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="29fa7-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="29fa7-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="29fa7-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="29fa7-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="29fa7-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="29fa7-143">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="29fa7-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="29fa7-144">Implementación de la tabla de visualización</span><span class="sxs-lookup"><span data-stu-id="29fa7-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="29fa7-145">Mostrar tablas</span><span class="sxs-lookup"><span data-stu-id="29fa7-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="29fa7-146">Información general del tipo de propiedad MAPI</span><span class="sxs-lookup"><span data-stu-id="29fa7-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

