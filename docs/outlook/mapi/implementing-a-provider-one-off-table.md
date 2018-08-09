---
title: Implementar una tabla puntual de proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 99146f93dcf634be6766f5c6fcc0d1c610b84d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817677"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="2815e-103">Implementar una tabla puntual de proveedor</span><span class="sxs-lookup"><span data-stu-id="2815e-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="2815e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2815e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2815e-105">MAPI llama al método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) de su proveedor cuando el usuario de una aplicación cliente agrega un destinatario a un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="2815e-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="2815e-106">Normalmente, los tipos de direcciones que se solicitó son únicos para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="2815e-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="2815e-107">Si el proveedor admite la creación de destinatarios, debe proporcionar una tabla de uso único que expone las plantillas para cada tipo de dirección del destinatario compatible.</span><span class="sxs-lookup"><span data-stu-id="2815e-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="2815e-108">Si su proveedor no admite la creación de destinatarios, devolver MAPI_E_NO_SUPPORT de la llamada **GetOneOffTable** .</span><span class="sxs-lookup"><span data-stu-id="2815e-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="2815e-109">MAPI normalmente se conserve que tabla de uso único de su proveedor abierta para la duración de la sesión, liberarlo sólo cuando un cliente llama del subsistema o (método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) ) de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2815e-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="2815e-110">MAPI se registra para las notificaciones en esta tabla, por lo que si se agregan o se eliminan las plantillas, pueden reflejarán estos cambios al usuario.</span><span class="sxs-lookup"><span data-stu-id="2815e-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="2815e-111">**Para implementar IABLogon::GetOneOffTable**</span><span class="sxs-lookup"><span data-stu-id="2815e-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="2815e-112">Compruebe el valor del parámetro flags, _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="2815e-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="2815e-113">Si se establece el indicador MAPI_UNICODE y su proveedor no admite Unicode, se producirá un error y devolver MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="2815e-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="2815e-114">Compruebe si ya se creó la tabla de uso único de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="2815e-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="2815e-115">Debido a que las tablas de uso único son normalmente estáticas, su proveedor nunca tiene que pasar por el proceso de creación de más de una vez.</span><span class="sxs-lookup"><span data-stu-id="2815e-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="2815e-116">Si ya existe una tabla, devuelve un puntero a ella.</span><span class="sxs-lookup"><span data-stu-id="2815e-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="2815e-117">Si todavía no existe una tabla de uso único, llame a **CreateTable** para crear uno.</span><span class="sxs-lookup"><span data-stu-id="2815e-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="2815e-118">Establezca las siguientes propiedades para las columnas en las filas de tabla:</span><span class="sxs-lookup"><span data-stu-id="2815e-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="2815e-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el nombre del tipo de destinatario que puede crear la plantilla.</span><span class="sxs-lookup"><span data-stu-id="2815e-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="2815e-120">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para el identificador de entrada para la plantilla de uso único.</span><span class="sxs-lookup"><span data-stu-id="2815e-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="2815e-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) para indicar el nivel de jerarquía en la visualización de la tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="2815e-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="2815e-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) en TRUE para indicar si la fila representa una plantilla y FALSE en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2815e-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="2815e-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para el tipo de dirección creado por la plantilla.</span><span class="sxs-lookup"><span data-stu-id="2815e-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="2815e-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) a DT_MAILUSER o cualquier otro valor que indica el tipo de presentación para la plantilla.</span><span class="sxs-lookup"><span data-stu-id="2815e-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="2815e-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) a un único valor binario.</span><span class="sxs-lookup"><span data-stu-id="2815e-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="2815e-126">Llame a [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) para modificar directamente en la tabla.</span><span class="sxs-lookup"><span data-stu-id="2815e-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="2815e-127">Llame a [ITableData::HrGetView](itabledata-hrgetview.md) para crear una implementación de interfaz **IMAPITable** para volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2815e-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

