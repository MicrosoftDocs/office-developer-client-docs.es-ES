---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816257"
---
# <a name="iolkenum"></a>IOlkEnum

Admite enumerar cuentas como objetos de [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) . 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
|Suministrado por:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Obtiene el número de cuentas en el enumerador.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Restablece el enumerador al principio.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Obtiene la cuenta siguiente en el enumerador.  <br/> |
|[Omitir](iolkenum-skip.md) <br/> |Omite un número especificado de cuentas en el enumerador.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta interfaz es devuelto por **IOlkAccountManager::EnumerateAccounts** cuando se obtiene un enumerador de cuentas. 
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

