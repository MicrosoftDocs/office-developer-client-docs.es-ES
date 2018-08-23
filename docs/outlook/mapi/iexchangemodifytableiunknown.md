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
ms.openlocfilehash: 51a83e1e28534cc237419d9c4ae475c1d719c5de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565077"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Admite el acceso a objetos de la tabla de Microsoft Exchange Server, específicamente el acceso del sistema controlan los objetos de la tabla de lista (SACL) y objetos de la tabla en las carpetas de Microsoft Exchange Server de la regla. Esta interfaz es similar a la [IMAPITable: IUnknown](imapitableiunknown.md) interfaz, pero se agrega compatibilidad para las estructuras específicas de Microsoft Exchange Server que se usan para controlar las SACL y reglas. 
  
|||
|:-----|:-----|
|Expuestos por:  <br/> |Ninguna  <br/> |
|Se implementa mediante:  <br/> |Objetos de la tabla de servidor  <br/> |
|Llamado por:  <br/> |MAPI y las aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IExchangeModifyTable  <br/> |
|Tipo de puntero:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Modelo de transacciones:  <br/> |Negocian  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |Devuelve información sobre el último error que se produjo en un objeto table.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Devuelve un puntero a una interfaz para un objeto de tabla MAPI.  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Actualiza un objeto de tabla MAPI.  <br/> |
   
|**Propiedades que se usan para modificar una tabla de reglas**|**Access**|
|:-----|:-----|
|**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
|**Propiedades que se usan para modificar una tabla SACL**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener la interfaz **IExchangeModifyTable** , llame al método MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en una propiedad de tipo pt Object en un objeto folder. Cuando se llama al método **OpenProperty** , pase el valor **IID_IExchangeModifyTable** en el parámetro _lpiid_ . 
  
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

