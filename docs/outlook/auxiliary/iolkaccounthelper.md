---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 3c28b1e8ab7e2d72d27cc6545b6ef57834ef5b6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816211"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

Proporciona funcionalidad auxiliar en la sesión MAPI actual para administrar las cuentas.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Suministrado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Placeholder1](iolkaccounthelper-placeholder1.md) <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |Obtiene el nombre del perfil de una cuenta.  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |Se abre una sesión MAPI y mantiene una referencia a la sesión para el Administrador de cuentas.  <br/> |
|[HandsOffSession](iolkaccounthelper-handsoffsession.md) <br/> |Libera el objeto de sesión MAPI que se ha devuelto por [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta interfaz se pasa al [IOlkAccountManager::Init](iolkaccountmanager-init.md) al inicializar el Administrador de cuentas. 
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

