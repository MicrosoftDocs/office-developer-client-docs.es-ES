---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322158"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

Proporciona funcionalidad auxiliar en la sesión MAPI actual para administrar cuentas.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Suministrado por:  <br/> |Client  <br/> |
|Identificador de interfaz:  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Placeholder1](iolkaccounthelper-placeholder1.md) <br/> | *Este miembro es un marcador de posición y no es compatible.*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |Obtiene el nombre de Perfil de una cuenta.  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |Abre una sesión MAPI y mantiene una referencia a la sesión del administrador de cuentas.  <br/> |
|[HandsOffSession](iolkaccounthelper-handsoffsession.md) <br/> |Libera el objeto de sesión MAPI devuelto por [IOlkAccountHelper:: GetMapiSession](iolkaccounthelper-getmapisession.md).  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta interfaz se pasa a [IOlkAccountManager:: init](iolkaccountmanager-init.md) al inicializar el administrador de cuentas. 
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

