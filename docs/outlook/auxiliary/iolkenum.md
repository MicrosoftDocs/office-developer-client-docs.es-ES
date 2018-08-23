---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 19ec67bf033859073e7685912196369b664f4a36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592692"
---
# <a name="iolkenum"></a>IOlkEnum

Admite enumerar cuentas como objetos de [IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) . 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
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
  
## <a name="see-also"></a>Recursos adicionales

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

