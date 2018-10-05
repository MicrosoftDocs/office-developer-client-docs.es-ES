---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389739"
---
# <a name="iolkenum"></a>IOlkEnum

Admite enumerar cuentas como objetos de [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) . 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
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

