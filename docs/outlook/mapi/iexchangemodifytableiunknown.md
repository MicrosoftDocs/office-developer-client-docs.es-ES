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
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418109"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Admite el acceso Microsoft Exchange Server objetos de tabla, específicamente objetos de tabla de lista de control de acceso del sistema (SACL) y objetos de tabla de reglas en Microsoft Exchange Server carpetas. Esta interfaz se asemeja Microsoft Exchange Server la interfaz [IMAPITable: IUnknown,](imapitableiunknown.md) pero agrega compatibilidad con estructuras específicas de Microsoft Exchange Server que se usan para controlar las SACL y las reglas. 
  
|||
|:-----|:-----|
|Expuesto por:  <br/> |Ninguno  <br/> |
|Implementado por:  <br/> |Objetos de tabla de servidor  <br/> |
|Llamado por:  <br/> |MAPI y aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IExchangeModifyTable  <br/> |
|Tipo de puntero:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Modelo de transacción:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |Devuelve información sobre el último error que se produjo en un objeto de tabla.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Devuelve un puntero a una interfaz para un objeto de tabla MAPI.  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Actualiza un objeto de tabla MAPI.  <br/> |
   
|**Propiedades usadas para modificar una tabla de reglas**|**Access**|
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
   
|**Propiedades usadas para modificar una tabla SACL**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener la **interfaz IExchangeModifyTable,** llame al método MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en una propiedad de tipo PT_OBJECT en un objeto de carpeta. Cuando llame al método **OpenProperty,** pase el valor **IID_IExchangeModifyTable** en el _parámetro lpiid._ 
  
## <a name="see-also"></a>Consulte también



[Interfaces MAPI](mapi-interfaces.md)

