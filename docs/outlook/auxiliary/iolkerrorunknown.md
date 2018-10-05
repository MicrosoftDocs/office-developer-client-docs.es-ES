---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: dc2fe6bbaf4515d5c5f5be694b15040bf03ef374
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384643"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Proporciona información adicional sobre el último error.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Suministrado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Obtiene una cadena de mensaje para el error especificado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta interfaz proporciona información adicional acerca de un error en [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md)y [IOlkAccount](iolkaccount.md). También es la interfaz base para **IOlkAccountManager**, **IOlkAccountNotify**y **IOlkAccount**. 
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)

