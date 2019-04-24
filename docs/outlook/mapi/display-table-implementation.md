---
title: Implementación de la tabla de visualización
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339952"
---
# <a name="display-table-implementation"></a><span data-ttu-id="bdcc4-103">Implementación de la tabla de visualización</span><span class="sxs-lookup"><span data-stu-id="bdcc4-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="bdcc4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdcc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdcc4-105">Una tabla de presentación se usa para mostrar una hoja de propiedades, un cuadro de diálogo especial compuesto por una o más páginas de propiedades con fichas dedicadas a mostrar y posiblemente editar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="bdcc4-106">Una tabla de visualización asociada a cada tabla de presentación es una implementación de [IAttach: IMAPIProp](iattachimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="bdcc4-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="bdcc4-107">La implementación de [IMAPIProp](imapipropiunknown.md) mantiene los datos de propiedad que se presentan en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="bdcc4-108">Las filas de una tabla de presentación representan los controles en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="bdcc4-109">La mayoría de los controles se pueden asociar con propiedades mantenidas con la implementación de **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="bdcc4-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="bdcc4-110">Cuando un usuario cambia el valor de un control modificable, se actualiza la propiedad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="bdcc4-111">Las columnas de una tabla de presentación representan propiedades del control, como su posición en la hoja de propiedades, su tipo, estructura asociada e identificador.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="bdcc4-112">Para obtener una lista completa de las columnas de la tabla de visualización necesarias, consulte [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bdcc4-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="bdcc4-113">MAPI muestra una hoja de propiedades al usuario de una aplicación cliente mediante la lectura de valores de propiedad de la implementación de **IMAPIProp** asociada con la tabla de presentación o de la tabla de presentación directamente.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="bdcc4-114">A medida que el usuario trabaja con la hoja de propiedades, cambiando valores en los controles, las llamadas MAPI [IMAPIProp:: SetProps](imapiprop-setprops.md) para guardar un control modificado si está establecida la marca DT_SET_IMMEDIATE del control.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="bdcc4-115">Para los controles sin la marca DT_SET_IMMEDIATE establecida, los cambios en las propiedades se guardan cuando el usuario cierra el cuadro de diálogo haciendo clic en el botón **Aceptar** o **aplicar ahora** .</span><span class="sxs-lookup"><span data-stu-id="bdcc4-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="bdcc4-116">Cuando se hace clic en uno de estos botones o en el botón **Cancelar** , MAPI quita la hoja de propiedades de la vista.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="bdcc4-117">MAPI obtiene acceso a la tabla de visualización mediante una llamada al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) en la implementación de **IMAPIProp** y solicitando la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) o la hereda en un llamada que ha realizado a MAPI, como [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="bdcc4-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="bdcc4-118">La primera técnica de acceso se usa cuando se solicita a los proveedores de la libreta de direcciones que muestren detalles sobre los usuarios de mensajería o las listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="bdcc4-119">Se produce el siguiente procesamiento:</span><span class="sxs-lookup"><span data-stu-id="bdcc4-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="bdcc4-120">Un cliente llama al método [IAddrBook::D etails](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="bdcc4-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="bdcc4-121">MAPI llama al método [IABLogon:: OpenEntry](iablogon-openentry.md) del proveedor de la libreta de direcciones para obtener acceso al usuario de mensajería que representa la entrada seleccionada.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="bdcc4-122">MAPI llama al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del usuario de mensajería para recuperar la propiedad **PR_DETAILS_TABLE** , la tabla de presentación del cuadro de diálogo Detalles.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="bdcc4-123">MAPI muestra el cuadro de diálogo, controla la interacción del usuario con la información y lo quita cuando el usuario ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="bdcc4-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="bdcc4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdcc4-124">See also</span></span>



[<span data-ttu-id="bdcc4-125">Proveedores de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="bdcc4-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

