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
ms.openlocfilehash: e0797364eb4ec24793f64bad2f4d838507c236e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571069"
---
# <a name="dtblbutton"></a><span data-ttu-id="38f19-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="38f19-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="38f19-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38f19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38f19-105">Contiene información sobre un control de botón para un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="38f19-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38f19-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="38f19-106">Header file:</span></span>  <br/> |<span data-ttu-id="38f19-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38f19-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="38f19-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="38f19-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="38f19-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="38f19-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="38f19-110">Members</span><span class="sxs-lookup"><span data-stu-id="38f19-110">Members</span></span>

 <span data-ttu-id="38f19-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="38f19-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="38f19-112">Posición en la memoria de la cadena de caracteres que se muestra en el botón.</span><span class="sxs-lookup"><span data-stu-id="38f19-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="38f19-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="38f19-113">**ulFlags**</span></span>
  
> <span data-ttu-id="38f19-114">Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="38f19-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="38f19-115">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="38f19-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="38f19-116">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="38f19-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="38f19-117">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="38f19-117">The label is in Unicode format.</span></span> <span data-ttu-id="38f19-118">Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="38f19-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="38f19-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="38f19-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="38f19-120">Etiqueta de propiedad de una propiedad de tipo pt Object que implementa la interfaz [IMAPIControl](imapicontroliunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="38f19-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="38f19-121">Cuando se hace clic en el botón, MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para la implementación de [IMAPIProp](imapipropiunknown.md) de la tabla para mostrar recuperar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="38f19-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="38f19-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38f19-122">Remarks</span></span>

<span data-ttu-id="38f19-123">Una estructura **DTBLBUTTON** describe un botón de un control que, al hacer clic, permite que un usuario comenzar una operación.</span><span class="sxs-lookup"><span data-stu-id="38f19-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="38f19-124">Normalmente, al hacer clic en un botón hace que un cuadro de diálogo modal que se mostrará o una tarea de programación va a invocar.</span><span class="sxs-lookup"><span data-stu-id="38f19-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="38f19-125">Proveedores de servicios pueden implementar algo a través de un control de botón.</span><span class="sxs-lookup"><span data-stu-id="38f19-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="38f19-126">Si se supone que el botón para realizar una tarea en función de los valores de otros controles, dichos controles deben ha establecido el indicador DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="38f19-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="38f19-127">El miembro **ulbLpszLabel** es la posición en la memoria de la cadena de caracteres que se muestra en el botón.</span><span class="sxs-lookup"><span data-stu-id="38f19-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="38f19-128">Proveedores de servicios pueden agregar un carácter de y comercial (&amp;) para indicar un acelerador de Windows en la etiqueta del botón.</span><span class="sxs-lookup"><span data-stu-id="38f19-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="38f19-129">Al presionar una tecla de aceleración tiene el mismo efecto que hacer clic en el botón.</span><span class="sxs-lookup"><span data-stu-id="38f19-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="38f19-130">El miembro **ulPRControl** describe una propiedad de objeto que, cuando se abre con el método **IMAPIProp::OpenProperty** , devuelve un puntero a un objeto de control.</span><span class="sxs-lookup"><span data-stu-id="38f19-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="38f19-131">Implementación de un objeto de control que admite la interfaz **IMAPIControl** es una forma de extender el conjunto de características MAPI y definir la operación o una tarea que se produce cuando se hace clic en el botón.</span><span class="sxs-lookup"><span data-stu-id="38f19-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="38f19-132">**IMAPIControl** proporciona dos métodos para manipular los botones: [GetState](imapicontrol-getstate.md) para deshabilitar o habilitar los botones y [Activar](imapicontrol-activate.md) para controlar los clics de botón.</span><span class="sxs-lookup"><span data-stu-id="38f19-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="38f19-133">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="38f19-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="38f19-134">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="38f19-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="38f19-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="38f19-135">See also</span></span>



[<span data-ttu-id="38f19-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="38f19-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="38f19-137">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="38f19-137">MAPI Structures</span></span>](mapi-structures.md)

