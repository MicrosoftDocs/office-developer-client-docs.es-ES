---
title: Implementación de la tabla para mostrar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 07ad94c423c3be425dc905dc578f55ad2c467a95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816675"
---
# <a name="display-table-implementation"></a><span data-ttu-id="d9df0-103">Implementación de la tabla para mostrar</span><span class="sxs-lookup"><span data-stu-id="d9df0-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="d9df0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9df0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9df0-105">Una tabla para mostrar se usa para mostrar una hoja de propiedades, un cuadro de diálogo especial que se compone de una o más páginas con fichas (propiedad) dedicado a mostrar y, posiblemente, editar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9df0-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="d9df0-106">Asociada con cada para mostrar tabla es un [IAttach: IMAPIProp](iattachimapiprop.md) implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="d9df0-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="d9df0-107">La implementación de [IMAPIProp](imapipropiunknown.md) mantiene los datos de propiedad que se presentan en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9df0-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="d9df0-108">Las filas de una tabla para mostrar representan los controles en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9df0-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="d9df0-109">La mayoría de los controles se pueden asociados con las propiedades que se mantiene con la implementación de **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="d9df0-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="d9df0-110">Cuando un usuario cambia el valor de un control modificable, se actualiza la propiedad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d9df0-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="d9df0-111">Las columnas de una tabla para mostrar representan las propiedades del control, como su posición en la hoja de propiedades, su tipo, estructura asociada e identificador.</span><span class="sxs-lookup"><span data-stu-id="d9df0-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="d9df0-112">Para obtener una lista completa de las columnas de tabla para mostrar necesarios, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d9df0-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="d9df0-113">MAPI muestra una hoja de propiedades para el usuario de una aplicación cliente mediante la lectura de los valores de propiedad desde la implementación de **IMAPIProp** asociado a la tabla para mostrar o desde la tabla para mostrar directamente.</span><span class="sxs-lookup"><span data-stu-id="d9df0-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="d9df0-114">Mientras el usuario trabaja con la hoja de propiedades, cambiar los valores de los controles MAPI llama a [IMAPIProp::SetProps](imapiprop-setprops.md) para guardar un control modificado si se establece la marca DT_SET_IMMEDIATE del control.</span><span class="sxs-lookup"><span data-stu-id="d9df0-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="d9df0-115">Para los controles sin establecer el indicador DT_SET_IMMEDIATE, se guardan los cambios realizados en las propiedades cuando el usuario cierra el cuadro de diálogo haciendo clic en el botón **Aceptar** o **Aplicar ahora** .</span><span class="sxs-lookup"><span data-stu-id="d9df0-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="d9df0-116">Cuando se hace clic en cualquiera de estos botones o el botón **Cancelar** , MAPI quita la hoja de propiedades de la vista.</span><span class="sxs-lookup"><span data-stu-id="d9df0-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="d9df0-117">MAPI obtiene acceso a la tabla para mostrar por llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en la implementación de **IMAPIProp** y solicitar la propiedad de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) o mediante la herencia de un llamada realizados en MAPI, como [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="d9df0-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="d9df0-118">La primera técnica de acceso se usa cuando los proveedores de la libreta de direcciones se le pida que mostrar detalles acerca de la mensajería a los usuarios o las listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="d9df0-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="d9df0-119">Se produce el procesamiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="d9df0-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="d9df0-120">Un cliente llama al método de [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="d9df0-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="d9df0-121">MAPI llama al método [IABLogon::OpenEntry](iablogon-openentry.md) del proveedor de libreta de direcciones para tener acceso el usuario de mensajería que representa la entrada seleccionada.</span><span class="sxs-lookup"><span data-stu-id="d9df0-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="d9df0-122">MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del usuario de mensajería para recuperar la propiedad **PR_DETAILS_TABLE** , en la tabla para mostrar para el cuadro de diálogo detalles.</span><span class="sxs-lookup"><span data-stu-id="d9df0-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="d9df0-123">Muestra el cuadro de diálogo, controlar la interacción del usuario con la información MAPI y lo quita cuando el usuario ha terminado.</span><span class="sxs-lookup"><span data-stu-id="d9df0-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d9df0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9df0-124">See also</span></span>



[<span data-ttu-id="d9df0-125">Proveedores de servicios de MAPI</span><span class="sxs-lookup"><span data-stu-id="d9df0-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

