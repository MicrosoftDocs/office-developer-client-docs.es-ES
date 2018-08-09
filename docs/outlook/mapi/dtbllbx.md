---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 04fbfb2e6938c1ae5971e90b30f5ef749e7963e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816735"
---
# <a name="dtbllbx"></a><span data-ttu-id="cba7d-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="cba7d-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="cba7d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cba7d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cba7d-105">Describe una lista que se usará en un cuadro de diálogo que se genera a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="cba7d-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cba7d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="cba7d-106">Header file:</span></span>  <br/> |<span data-ttu-id="cba7d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cba7d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="cba7d-108">Members</span><span class="sxs-lookup"><span data-stu-id="cba7d-108">Members</span></span>

 <span data-ttu-id="cba7d-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="cba7d-109">**ulFlags**</span></span>
  
> <span data-ttu-id="cba7d-110">Máscara de bits de marcas que se usan para eliminar una barra de desplazamiento horizontal o vertical de la lista.</span><span class="sxs-lookup"><span data-stu-id="cba7d-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="cba7d-111">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="cba7d-111">The following flags can be set:</span></span>
    
<span data-ttu-id="cba7d-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="cba7d-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="cba7d-113">No debe ser se muestra ninguna barra de desplazamiento horizontal con la lista.</span><span class="sxs-lookup"><span data-stu-id="cba7d-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="cba7d-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="cba7d-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="cba7d-115">No debe ser se muestra ninguna barra de desplazamiento vertical con la lista.</span><span class="sxs-lookup"><span data-stu-id="cba7d-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="cba7d-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="cba7d-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="cba7d-117">Etiqueta de propiedad de una propiedad de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="cba7d-117">Property tag for a property of any type.</span></span> <span data-ttu-id="cba7d-118">Esta propiedad es una de las columnas en la tabla identificada por el miembro **ulPRTableTable** .</span><span class="sxs-lookup"><span data-stu-id="cba7d-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="cba7d-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="cba7d-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="cba7d-120">Etiqueta de la propiedad para una propiedad de tabla de tipo pt Object que se pueden abrir mediante el uso de un **OpenProperty** llamar.</span><span class="sxs-lookup"><span data-stu-id="cba7d-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="cba7d-121">El número de columnas que debería tener la tabla depende de si la lista es una lista de selección múltiple o simple.</span><span class="sxs-lookup"><span data-stu-id="cba7d-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="cba7d-122">Si se establece el miembro **ulPRSetProperty** en **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), la lista permite la selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="cba7d-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cba7d-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cba7d-123">Remarks</span></span>

<span data-ttu-id="cba7d-124">Una estructura **DTBLLBX** describe un un control que se usa para mostrar varios elementos y permitir que un usuario seleccione uno o varios de los elementos de lista.</span><span class="sxs-lookup"><span data-stu-id="cba7d-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="cba7d-125">El miembro **ulPRSetProperty** y **ulPRTableName** miembro funcionan conjuntamente; Cuando se elige un valor de la tabla, está escrito volver a **ulPRSetProperty** cuando se cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cba7d-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="cba7d-126">El valor de flags indica si se debe mostrar una barra de desplazamiento horizontal o vertical con la lista.</span><span class="sxs-lookup"><span data-stu-id="cba7d-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="cba7d-127">El valor predeterminado es a tener tipos de muestran barras de desplazamiento si es necesario.</span><span class="sxs-lookup"><span data-stu-id="cba7d-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="cba7d-128">Proveedores de servicios pueden establecer MAPI_NO_HBAR para suprimir una barra de desplazamiento horizontal y MAPI_NO_VBAR para suprimir una barra de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="cba7d-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="cba7d-129">Los miembros de la etiqueta de dos propiedad funcionan conjuntamente para mostrar los valores en la lista y establecer las propiedades correspondientes cuando se selecciona un elemento en la lista.</span><span class="sxs-lookup"><span data-stu-id="cba7d-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="cba7d-130">Cuando MAPI en primer lugar muestra la lista, se llama el **IMAPIProp** **OpenProperty** método de la implementación para recuperar la tabla identificada en el miembro **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="cba7d-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="cba7d-131">El número de columnas de la tabla depende del valor del miembro **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="cba7d-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="cba7d-132">Si **ulPRSetProperty** se establece en **PR_NULL**, la lista es una lista de selección de varios basándose en un objeto que contiene a los destinatarios, como un contenedor de la libreta de direcciones, una tabla de destinatarios para un mensaje o una tabla de contenido de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="cba7d-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="cba7d-133">Una tabla para una lista de selección múltiple debe incluir las siguientes columnas:</span><span class="sxs-lookup"><span data-stu-id="cba7d-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="cba7d-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cba7d-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="cba7d-135">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cba7d-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="cba7d-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cba7d-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="cba7d-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) y también se puede mostrar un máximo de cinco otras propiedades de cadena multivalor con las tres columnas necesarias.</span><span class="sxs-lookup"><span data-stu-id="cba7d-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="cba7d-138">Si el miembro **ulPRSetProperty** no está establecido en **PR_NULL**, la lista es una lista de selección única.</span><span class="sxs-lookup"><span data-stu-id="cba7d-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="cba7d-139">El valor inicial de **ulPRSetProperty** determina la primera fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="cba7d-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="cba7d-140">Cuando un usuario selecciona una de las filas, el miembro **ulPRSetProperty** se establece en el valor seleccionado y este valor se vuelve a escribir la implementación de la interfaz de propiedad con una llamada a [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="cba7d-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="cba7d-141">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cba7d-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="cba7d-142">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="cba7d-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cba7d-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="cba7d-143">See also</span></span>



[<span data-ttu-id="cba7d-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="cba7d-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="cba7d-145">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="cba7d-145">MAPI Structures</span></span>](mapi-structures.md)

