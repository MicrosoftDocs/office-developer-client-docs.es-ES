---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: 311d055e0a319ec26cdc4eba5ac3b50dc9e63d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565182"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Proporciona información adicional sobre el último error.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Suministrado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Obtiene una cadena de mensaje para el error especificado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta interfaz proporciona información adicional acerca de un error en [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md)y [IOlkAccount](iolkaccount.md). También es la interfaz base para **IOlkAccountManager**, **IOlkAccountNotify**y **IOlkAccount**. 
  
## <a name="see-also"></a>Recursos adicionales

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)

