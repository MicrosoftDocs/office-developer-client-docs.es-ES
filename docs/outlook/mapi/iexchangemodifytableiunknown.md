---
title: IExchangeModifyTable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1093975e6cbdd79004125a0a4a3098ffa421ab0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817185"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="ddf1f-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ddf1f-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="ddf1f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ddf1f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ddf1f-105">Admite el acceso a objetos de la tabla de Microsoft Exchange Server, específicamente el acceso del sistema controlan los objetos de la tabla de lista (SACL) y objetos de la tabla en las carpetas de Microsoft Exchange Server de la regla.</span><span class="sxs-lookup"><span data-stu-id="ddf1f-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="ddf1f-106">Esta interfaz es similar a la [IMAPITable: IUnknown](imapitableiunknown.md) interfaz, pero se agrega compatibilidad para las estructuras específicas de Microsoft Exchange Server que se usan para controlar las SACL y reglas.</span><span class="sxs-lookup"><span data-stu-id="ddf1f-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddf1f-107">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="ddf1f-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="ddf1f-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ddf1f-108">None</span></span>  <br/> |
|<span data-ttu-id="ddf1f-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ddf1f-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="ddf1f-110">Objetos de la tabla de servidor</span><span class="sxs-lookup"><span data-stu-id="ddf1f-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="ddf1f-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ddf1f-111">Called by:</span></span>  <br/> |<span data-ttu-id="ddf1f-112">MAPI y las aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="ddf1f-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="ddf1f-113">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="ddf1f-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ddf1f-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="ddf1f-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="ddf1f-115">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="ddf1f-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="ddf1f-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="ddf1f-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="ddf1f-117">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="ddf1f-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="ddf1f-118">Negocian</span><span class="sxs-lookup"><span data-stu-id="ddf1f-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ddf1f-119">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="ddf1f-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ddf1f-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="ddf1f-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="ddf1f-121">Devuelve información sobre el último error que se produjo en un objeto table.</span><span class="sxs-lookup"><span data-stu-id="ddf1f-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="ddf1f-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="ddf1f-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="ddf1f-123">Devuelve un puntero a una interfaz para un objeto de tabla MAPI.</span><span class="sxs-lookup"><span data-stu-id="ddf1f-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="ddf1f-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="ddf1f-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="ddf1f-125">Actualiza un objeto de tabla MAPI.</span><span class="sxs-lookup"><span data-stu-id="ddf1f-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="ddf1f-126">**Propiedades que se usan para modificar una tabla de reglas**</span><span class="sxs-lookup"><span data-stu-id="ddf1f-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="ddf1f-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="ddf1f-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ddf1f-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="ddf1f-148">**Propiedades que se usan para modificar una tabla SACL**</span><span class="sxs-lookup"><span data-stu-id="ddf1f-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="ddf1f-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="ddf1f-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ddf1f-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-151">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-155">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="ddf1f-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ddf1f-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ddf1f-157">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddf1f-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddf1f-158">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ddf1f-158">Remarks</span></span>

<span data-ttu-id="ddf1f-159">Para obtener la interfaz **IExchangeModifyTable** , llame al método MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en una propiedad de tipo pt Object en un objeto folder.</span><span class="sxs-lookup"><span data-stu-id="ddf1f-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="ddf1f-160">Cuando se llama al método **OpenProperty** , pase el valor **IID_IExchangeModifyTable** en el parámetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="ddf1f-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ddf1f-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddf1f-161">See also</span></span>



[<span data-ttu-id="ddf1f-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ddf1f-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

