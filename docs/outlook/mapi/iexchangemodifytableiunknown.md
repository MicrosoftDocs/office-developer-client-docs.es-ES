---
title: IUnknown IExchangeModifyTable
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
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350886"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="249a2-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="249a2-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="249a2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="249a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="249a2-105">Admite el acceso a objetos de tabla de Microsoft Exchange Server, en concreto objetos de tabla de lista de control de acceso del sistema (SACL) y objetos de tabla de reglas en carpetas de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="249a2-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="249a2-106">Esta interfaz es similar a la interfaz [IMAPITable: IUnknown](imapitableiunknown.md) , pero agrega compatibilidad para las estructuras específicas de Microsoft Exchange Server que se usan para controlar las SACL y las reglas.</span><span class="sxs-lookup"><span data-stu-id="249a2-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="249a2-107">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="249a2-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="249a2-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="249a2-108">None</span></span>  <br/> |
|<span data-ttu-id="249a2-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="249a2-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="249a2-110">Objetos de tabla de servidor</span><span class="sxs-lookup"><span data-stu-id="249a2-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="249a2-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="249a2-111">Called by:</span></span>  <br/> |<span data-ttu-id="249a2-112">MAPI y aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="249a2-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="249a2-113">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="249a2-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="249a2-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="249a2-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="249a2-115">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="249a2-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="249a2-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="249a2-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="249a2-117">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="249a2-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="249a2-118">Negocian</span><span class="sxs-lookup"><span data-stu-id="249a2-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="249a2-119">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="249a2-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="249a2-120">Volvió</span><span class="sxs-lookup"><span data-stu-id="249a2-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="249a2-121">Devuelve información sobre el último error que se produjo en un objeto Table.</span><span class="sxs-lookup"><span data-stu-id="249a2-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="249a2-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="249a2-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="249a2-123">Devuelve un puntero a una interfaz para un objeto Table de MAPI.</span><span class="sxs-lookup"><span data-stu-id="249a2-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="249a2-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="249a2-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="249a2-125">Actualiza un objeto de tabla MAPI.</span><span class="sxs-lookup"><span data-stu-id="249a2-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="249a2-126">**Propiedades usadas para modificar una tabla rules**</span><span class="sxs-lookup"><span data-stu-id="249a2-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="249a2-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="249a2-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="249a2-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="249a2-148">**Propiedades usadas para modificar una tabla de SACL**</span><span class="sxs-lookup"><span data-stu-id="249a2-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="249a2-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="249a2-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="249a2-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-151">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-155">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="249a2-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="249a2-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="249a2-157">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="249a2-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="249a2-158">Comentarios</span><span class="sxs-lookup"><span data-stu-id="249a2-158">Remarks</span></span>

<span data-ttu-id="249a2-159">Para obtener la interfaz **IExchangeModifyTable** , llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) de MAPI en una propiedad de tipo PT Object en un objeto Folder.</span><span class="sxs-lookup"><span data-stu-id="249a2-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="249a2-160">Cuando se llama al método **OpenProperty** , se pasa el valor **IID_IExchangeModifyTable** en el parámetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="249a2-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="249a2-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="249a2-161">See also</span></span>



[<span data-ttu-id="249a2-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="249a2-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

