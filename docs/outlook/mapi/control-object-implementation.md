---
title: Administrar la implementación de objeto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b4b225f7e048ef40a79c4b258629cb01b79368d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565833"
---
# <a name="control-object-implementation"></a><span data-ttu-id="40297-103">Administrar la implementación de objeto</span><span class="sxs-lookup"><span data-stu-id="40297-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="40297-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40297-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40297-105">Controlar objetos u objetos que admiten la [IMAPIControl: IUnknown](imapicontroliunknown.md) de la interfaz, se implementan los proveedores para agregar funcionalidad a un botón que aparece en un cuadro de diálogo MAPI.</span><span class="sxs-lookup"><span data-stu-id="40297-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="40297-106">Objetos de control sólo se pueden implementar para los botones.</span><span class="sxs-lookup"><span data-stu-id="40297-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="40297-107">**IMAPIControl** tiene tres métodos: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)y [Activar](imapicontrol-activate.md).</span><span class="sxs-lookup"><span data-stu-id="40297-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="40297-108">MAPI llama **GetState** para determinar si desea deshabilitar el botón o no.</span><span class="sxs-lookup"><span data-stu-id="40297-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="40297-109">Se denomina **GetState** en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="40297-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="40297-110">Cuando el cuadro de diálogo en el que aparece el botón aparece por primera vez.</span><span class="sxs-lookup"><span data-stu-id="40297-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="40297-111">Cuando se emite una notificación de la tabla para mostrar para el botón.</span><span class="sxs-lookup"><span data-stu-id="40297-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="40297-112">Establecer el contenido del parámetro _lpulState_ a MAPI_DISABLED si el usuario no puede interactuar con el botón y MAPI_ENABLED si el usuario puede interactuar.</span><span class="sxs-lookup"><span data-stu-id="40297-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="40297-113">Cuando el usuario hace clic en el botón, MAPI llama a **Activar**.</span><span class="sxs-lookup"><span data-stu-id="40297-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="40297-114">**Activar** lleva a cabo la tarea que se ha asociado con el botón.</span><span class="sxs-lookup"><span data-stu-id="40297-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="40297-115">Esta tarea puede ser cualquier cosa apropiada para su proveedor, como mostrar un cuadro de diálogo o actualización de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="40297-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="40297-116">Si la tarea es incorrecta debido a que el usuario se ha cancelado, devolver MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="40297-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="40297-117">Para otras causas de error, devuelve el valor de error apropiado.</span><span class="sxs-lookup"><span data-stu-id="40297-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="40297-118">Si la tarea se realiza correctamente y se vincula a un cambio de propiedad que se refleja en otro control en el cuadro de diálogo, llame a [ITableData::HrNotify](itabledata-hrnotify.md).</span><span class="sxs-lookup"><span data-stu-id="40297-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="40297-119">**HrNotify** se llama para emitir una notificación de la tabla para mostrar con la propiedad de **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) de la propiedad modificada en la estructura [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="40297-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="40297-120">El nuevo valor de propiedad no se coloca en la estructura; en su lugar, devolver cuando se llama a [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="40297-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="40297-121">Aunque normalmente no se puede usar una notificación de la tabla para mostrar para deshabilitar o habilitar un control, se puede utilizar con un botón.</span><span class="sxs-lookup"><span data-stu-id="40297-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="40297-122">MAPI actualizará el control modificado para responder a la notificación.</span><span class="sxs-lookup"><span data-stu-id="40297-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="40297-123">MAPI llama al método del control **GetLastError** al **Activar** devuelve un error que no sea MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="40297-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="40297-124">Si **GetLastError** coloca información de error extendida en la estructura [MAPIERROR](mapierror.md) que devuelve en el contenido del parámetro _lppMAPIError_ , MAPI muestra para el usuario.</span><span class="sxs-lookup"><span data-stu-id="40297-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40297-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="40297-125">See also</span></span>



[<span data-ttu-id="40297-126">Proveedores de servicios de MAPI</span><span class="sxs-lookup"><span data-stu-id="40297-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

