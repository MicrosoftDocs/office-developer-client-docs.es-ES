---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322102"
---
# <a name="iolkenum"></a>IOlkEnum

Admite la enumeración de cuentas como [objetos IUnknown.](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Suministrado por:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Obtiene el número de cuentas del enumerador.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Restablece el enumerador al principio.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Obtiene la siguiente cuenta en el enumerador.  <br/> |
|[Skip](iolkenum-skip.md) <br/> |Omite un número especificado de cuentas en el enumerador.  <br/> |
   
## <a name="remarks"></a>Comentarios

**IOlkAccountManager::EnumerateAccounts** devuelve esta interfaz al obtener un enumerador de cuentas. 
  
## <a name="see-also"></a>Consulte también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

