---
title: Uso de las herramientas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409989"
---
# <a name="using-the-mapi-utilities"></a>Uso de las herramientas MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las utilidades MAPI se componen de datos de tabla y objetos de datos de propiedad, y una variedad de funciones para admitir varias características. Es posible que un cliente solo necesite estas herramientas y que no tenga que iniciar sesión en el subsistema MAPI para establecer una conexión con los proveedores de servicios. Si el cliente encaja en esta categoría, llame a la función de la API [ScInitMapiUtil](scinitmapiutil.md) en lugar de la función [MAPIInitialize](mapiinitialize.md) en el momento de la inicialización. 
  
 **ScInitMapiUtil** permite a los clientes usar funciones de utilidad que requieren asignadores MAPI, pero que no solicitan los asignadores de forma explícita. Cuando sea el momento de apagar, llame a [DeinitMapiUtil](deinitmapiutil.md) para liberar recursos en lugar de [MAPIUninitialize](mapiuninitialize.md). Los clientes que nunca llaman a **MAPIInitialize** no deben llamar a **MAPIUninitialize**.
  
Si ha llamado **ScInitMapiUtil** en lugar de **MAPIInitialize** y está usando tablas a través de los métodos de **ITableData** en lugar de los métodos **IMAPITable** , tenga en cuenta que las notificaciones de tabla no funcionarán. Las notificaciones requieren el uso de las bibliotecas MAPI y el [IMAPITable: IUnknown](imapitableiunknown.md).
  

