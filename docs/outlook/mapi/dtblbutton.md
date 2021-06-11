---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412789"
---
# <a name="dtblbutton"></a><span data-ttu-id="f0f67-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="f0f67-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="f0f67-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0f67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0f67-105">Contiene información sobre un control de botón para un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="f0f67-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0f67-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f0f67-106">Header file:</span></span>  <br/> |<span data-ttu-id="f0f67-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0f67-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f0f67-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="f0f67-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="f0f67-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="f0f67-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="f0f67-110">Members</span><span class="sxs-lookup"><span data-stu-id="f0f67-110">Members</span></span>

 <span data-ttu-id="f0f67-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="f0f67-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="f0f67-112">Posición en la memoria de la cadena de caracteres que se muestra en el botón.</span><span class="sxs-lookup"><span data-stu-id="f0f67-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="f0f67-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f0f67-113">**ulFlags**</span></span>
  
> <span data-ttu-id="f0f67-114">Máscara de bits de las marcas usadas para designar el formato de la etiqueta señalada por el **miembro ulbLpszLabel.**</span><span class="sxs-lookup"><span data-stu-id="f0f67-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="f0f67-115">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="f0f67-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="f0f67-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0f67-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f0f67-117">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0f67-117">The label is in Unicode format.</span></span> <span data-ttu-id="f0f67-118">Si la MAPI_UNICODE no está establecida, la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f0f67-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="f0f67-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="f0f67-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="f0f67-120">Etiqueta de propiedad para una propiedad de tipo PT_OBJECT que implementa la [interfaz IMAPIControl.](imapicontroliunknown.md)</span><span class="sxs-lookup"><span data-stu-id="f0f67-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="f0f67-121">Cuando se hace clic en el botón, MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para que la implementación [IMAPIProp](imapipropiunknown.md) de la tabla para mostrar recupere esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f0f67-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f0f67-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0f67-122">Remarks</span></span>

<span data-ttu-id="f0f67-123">Una **estructura DTBLBUTTON** describe un botón un control que, al hacer clic, permite al usuario iniciar una operación.</span><span class="sxs-lookup"><span data-stu-id="f0f67-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="f0f67-124">Normalmente, al hacer clic en un botón, se muestra un cuadro de diálogo modal o se invoca una tarea mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f0f67-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="f0f67-125">Los proveedores de servicios pueden implementar cualquier cosa a través de un control de botón.</span><span class="sxs-lookup"><span data-stu-id="f0f67-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="f0f67-126">Si se supone que el botón debe realizar una tarea en función de los valores de otros controles, estos controles deben haber establecido la marca DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="f0f67-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="f0f67-127">El **miembro ulbLpszLabel** es la posición en la memoria de la cadena de caracteres que se muestra en el botón.</span><span class="sxs-lookup"><span data-stu-id="f0f67-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="f0f67-128">Los proveedores de servicios pueden agregar un carácter de yerba ( ) para indicar &amp; un Windows acelerador en la etiqueta del botón.</span><span class="sxs-lookup"><span data-stu-id="f0f67-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="f0f67-129">Presionar una tecla de aceleración tiene el mismo efecto que hacer clic en el botón.</span><span class="sxs-lookup"><span data-stu-id="f0f67-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="f0f67-130">El **miembro ulPRControl** describe una propiedad de objeto que, cuando se abre con el método **IMAPIProp::OpenProperty,** devuelve un puntero a un objeto de control.</span><span class="sxs-lookup"><span data-stu-id="f0f67-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="f0f67-131">La implementación de un objeto de control compatible con la interfaz **IMAPIControl** es una forma de ampliar el conjunto de características MAPI y definir la operación o tarea que se produce cuando se hace clic en el botón.</span><span class="sxs-lookup"><span data-stu-id="f0f67-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="f0f67-132">**IMAPIControl proporciona** dos métodos para manipular botones: [GetState](imapicontrol-getstate.md) para deshabilitar o habilitar botones y [Activar](imapicontrol-activate.md) para controlar los clics de botón.</span><span class="sxs-lookup"><span data-stu-id="f0f67-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="f0f67-133">Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="f0f67-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="f0f67-134">Para obtener información sobre cómo implementar una tabla para mostrar, vea [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="f0f67-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f0f67-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0f67-135">See also</span></span>



[<span data-ttu-id="f0f67-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="f0f67-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="f0f67-137">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="f0f67-137">MAPI Structures</span></span>](mapi-structures.md)

