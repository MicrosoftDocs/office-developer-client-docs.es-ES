---
title: Mostrar la información del destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412958"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="5648e-103">Mostrar la información del destinatario</span><span class="sxs-lookup"><span data-stu-id="5648e-103">Displaying recipient information</span></span>

<span data-ttu-id="5648e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5648e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5648e-105">MAPI proporciona un cuadro de diálogo común para mostrar los detalles del destinatario.</span><span class="sxs-lookup"><span data-stu-id="5648e-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="5648e-106">El cuadro de diálogo de detalles se crea a partir de una tabla para mostrar y una **implementación de IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="5648e-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="5648e-107">La tabla para mostrar describe la apariencia de la presentación de detalles y la implementación **de IMAPIProp** controla los datos del destinatario.</span><span class="sxs-lookup"><span data-stu-id="5648e-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="5648e-108">El proveedor es responsable de proporcionar la tabla para mostrar y la **implementación de IMAPIProp** para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="5648e-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="5648e-109">La forma más sencilla de crear la tabla para mostrar es definir una [estructura DTPAGE](dtpage.md) y llamar a [BuildDisplayTable](builddisplaytable.md).</span><span class="sxs-lookup"><span data-stu-id="5648e-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="5648e-110">Sin embargo, algunos proveedores, específicamente proveedores de solo lectura que permiten la creación de destinatarios únicos, usan **IPropData**.</span><span class="sxs-lookup"><span data-stu-id="5648e-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="5648e-111">La **implementación de IMAPIProp** puede ser cualquier tipo de objeto de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5648e-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="5648e-112">Hay dos métodos para invocar este cuadro de diálogo: [IAddrBook::D etails](iaddrbook-details.md) e [IMAPISupport::D etails](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="5648e-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="5648e-113">Cuando el proveedor llama a uno de estos métodos para solicitar detalles para un destinatario, MAPI primero abre el destinatario llamando al método [IMAPIContainer::OpenEntry de](imapicontainer-openentry.md) su contenedor.</span><span class="sxs-lookup"><span data-stu-id="5648e-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="5648e-114">A continuación, llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del destinatario para solicitar la **propiedad PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5648e-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="5648e-115">**PR_DETAILS_TABLE** es la propiedad que representa la tabla para mostrar detalles de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="5648e-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="5648e-116">La [interfaz IPropData : IMAPIProp](ipropdataimapiprop.md) se puede usar para supervisar los cambios en los controles de tabla para mostrar, tal como se describe en el siguiente procedimiento.</span><span class="sxs-lookup"><span data-stu-id="5648e-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="5648e-117">Supervisar cambios en un control</span><span class="sxs-lookup"><span data-stu-id="5648e-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="5648e-118">Antes de que el usuario obtenga acceso al control, llame a [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) para establecer el acceso del control a IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="5648e-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="5648e-119">Permitir que el usuario trabaje con el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5648e-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="5648e-120">Cuando el usuario haya terminado, llame a [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) para recuperar el nivel de acceso actual del control.</span><span class="sxs-lookup"><span data-stu-id="5648e-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="5648e-121">Si el nivel de acceso IPROP_DIRTY, el usuario ha modificado el control.</span><span class="sxs-lookup"><span data-stu-id="5648e-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="5648e-122">El proveedor debe:</span><span class="sxs-lookup"><span data-stu-id="5648e-122">Your provider should:</span></span>
    
   - <span data-ttu-id="5648e-123">Llame [a IPropData::HrSetPropAccess para](ipropdata-hrsetpropaccess.md) volver a establecer el nivel de acceso en IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="5648e-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="5648e-124">Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del objeto de datos de propiedad para recuperar la propiedad modificada y actualizarla llamando a [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="5648e-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="5648e-125">Si el nivel de acceso sigue IPROP_CLEAN, el control no se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="5648e-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="5648e-126">Para obtener más información acerca de la creación de tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5648e-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

