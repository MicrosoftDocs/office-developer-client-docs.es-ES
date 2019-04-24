---
title: Implementación de una tabla de un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332868"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="4647c-103">Implementación de una tabla de un proveedor</span><span class="sxs-lookup"><span data-stu-id="4647c-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="4647c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4647c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4647c-105">MAPI llama al método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) del proveedor cuando el usuario de una aplicación cliente agrega un destinatario a un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="4647c-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="4647c-106">Normalmente, los tipos de direcciones que se solicitan son únicos para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4647c-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="4647c-107">Si el proveedor admite la creación de destinatarios, debe proporcionar una tabla única que exponga las plantillas para cada tipo de dirección de destinatario compatible.</span><span class="sxs-lookup"><span data-stu-id="4647c-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="4647c-108">Si su proveedor no admite la creación de destinatarios, devuelva MAPI_E_NO_SUPPORT de la llamada a **GetOneOffTable** .</span><span class="sxs-lookup"><span data-stu-id="4647c-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="4647c-109">MAPI suele mantener abierta la tabla única del proveedor durante el período de duración de la sesión, que la libera solo cuando un cliente llama al método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) de la libreta de direcciones o del subsistema.</span><span class="sxs-lookup"><span data-stu-id="4647c-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="4647c-110">MAPI registra las notificaciones en esta tabla de modo que, si se agregan o se eliminan plantillas, estos cambios se pueden reflejar en el usuario.</span><span class="sxs-lookup"><span data-stu-id="4647c-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="4647c-111">**Para implementar IABLogon:: GetOneOffTable**</span><span class="sxs-lookup"><span data-stu-id="4647c-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="4647c-112">Compruebe el valor del parámetro flags, _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="4647c-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="4647c-113">Si se establece la marca MAPI_UNICODE y el proveedor no admite Unicode, se produce un error y se devuelve MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="4647c-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="4647c-114">Compruebe si ya se ha creado la tabla de uso único del proveedor.</span><span class="sxs-lookup"><span data-stu-id="4647c-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="4647c-115">Como las tablas de uso único suelen ser estáticas, el proveedor nunca tiene que pasar por el proceso de creación más de una vez.</span><span class="sxs-lookup"><span data-stu-id="4647c-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="4647c-116">Si ya existe una tabla, devuelva un puntero a ella.</span><span class="sxs-lookup"><span data-stu-id="4647c-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="4647c-117">Si aún no existe una tabla de uso único, llame a **createTable** para crear una.</span><span class="sxs-lookup"><span data-stu-id="4647c-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="4647c-118">Establezca las siguientes propiedades para las columnas de las filas de la tabla:</span><span class="sxs-lookup"><span data-stu-id="4647c-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="4647c-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el nombre del tipo de destinatario que la plantilla puede crear.</span><span class="sxs-lookup"><span data-stu-id="4647c-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="4647c-120">\*\*\*\* Es ([PidTagEntryId](pidtagentryid-canonical-property.md)) al identificador de entrada de la plantilla única.</span><span class="sxs-lookup"><span data-stu-id="4647c-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="4647c-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) para indicar el nivel de jerarquía en la visualización de la tabla de un solo uso.</span><span class="sxs-lookup"><span data-stu-id="4647c-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="4647c-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) en true para indicar si la fila representa una plantilla y false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4647c-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="4647c-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) al tipo de dirección creada por la plantilla.</span><span class="sxs-lookup"><span data-stu-id="4647c-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="4647c-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) a DT_MAILUSER u otro valor que indique el tipo de presentación de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="4647c-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="4647c-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) a un valor binario único.</span><span class="sxs-lookup"><span data-stu-id="4647c-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="4647c-126">Llame a [ITableData:: HrModifyRow](itabledata-hrmodifyrow.md) para modificar la tabla directamente.</span><span class="sxs-lookup"><span data-stu-id="4647c-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="4647c-127">Llame a [ITableData:: HrGetView](itabledata-hrgetview.md) para crear una implementación de la interfaz **IMAPITable** para volver a la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="4647c-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

