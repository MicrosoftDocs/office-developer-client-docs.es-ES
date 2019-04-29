---
title: Control de la implementación de objetos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422610"
---
# <a name="control-object-implementation"></a><span data-ttu-id="3c8b9-103">Control de la implementación de objetos</span><span class="sxs-lookup"><span data-stu-id="3c8b9-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="3c8b9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c8b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c8b9-105">Los proveedores implementan objetos de control, o objetos que admiten la interfaz [IMAPIControl: IUnknown](imapicontroliunknown.md) , para agregar funciones a un botón que aparece en un cuadro de diálogo MAPI.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="3c8b9-106">Los objetos de control solo se pueden implementar para botones.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="3c8b9-107">**IMAPIControl** tiene tres métodos: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)y [Activate](imapicontrol-activate.md).</span><span class="sxs-lookup"><span data-stu-id="3c8b9-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="3c8b9-108">MAPI llama a **GetState** para determinar si se va a deshabilitar el botón.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="3c8b9-109">Se llama a **GetState** en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="3c8b9-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="3c8b9-110">Cuando aparezca el cuadro de diálogo en el que aparece el botón por primera vez.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="3c8b9-111">Cuando se emite una notificación de tabla de presentación para el botón.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="3c8b9-112">Establezca el contenido del parámetro _lpulState_ en MAPI_DISABLED si el usuario no puede interactuar con el botón y MAPI_ENABLED si el usuario puede interactuar.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="3c8b9-113">Cuando el usuario hace clic en el botón, las \*\*\*\* llamadas MAPI se activan.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="3c8b9-114">**Activate** realiza la tarea que se ha asociado con el botón.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="3c8b9-115">Esta tarea puede ser cualquier cosa adecuada para su proveedor, como mostrar un cuadro de diálogo o actualizar una propiedad.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="3c8b9-116">Si la tarea no se realiza correctamente porque el usuario la ha cancelado, devuelve MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="3c8b9-117">Para otras causas de error, devuelva el valor de error apropiado.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="3c8b9-118">Si la tarea se realiza correctamente y está vinculada a un cambio de propiedad que se refleja en otro control del cuadro de diálogo, llame a [ITableData:: HrNotify](itabledata-hrnotify.md).</span><span class="sxs-lookup"><span data-stu-id="3c8b9-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="3c8b9-119">Se llama a **HrNotify** para emitir una notificación de tabla de presentación con la propiedad **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) de la propiedad modificada en la estructura [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="3c8b9-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="3c8b9-120">No ponga el nuevo valor de la propiedad en la estructura; en su lugar, devuelva este método cuando se llama a [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="3c8b9-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="3c8b9-121">Aunque normalmente no se puede usar una notificación de tabla de visualización para deshabilitar o habilitar un control, se puede usar con un botón.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="3c8b9-122">MAPI actualizará el control cambiado para responder a la notificación.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="3c8b9-123">MAPI llama al método **GetLastError** del control cuando **Activate** devuelve un error distinto de MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="3c8b9-124">Si **GetLastError** coloca información de error extendida en la estructura [MAPIERROR](mapierror.md) que devuelve en el contenido del parámetro _lppMAPIError_ , MAPI la muestra para el usuario.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c8b9-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="3c8b9-125">See also</span></span>



[<span data-ttu-id="3c8b9-126">Proveedores de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="3c8b9-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

