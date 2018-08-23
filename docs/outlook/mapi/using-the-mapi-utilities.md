---
title: Usar las herramientas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4612b6f345d59d988013671758c6d0579aaa127d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569536"
---
# <a name="using-the-mapi-utilities"></a>Usar las herramientas MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las utilidades MAPI se componen de datos de la tabla y objetos de datos de propiedad y una gran variedad de funciones para admitir las características varias. Es posible que un cliente necesita sólo estas utilidades y no tiene que iniciar sesión en el subsistema MAPI para establecer una conexión con los proveedores de servicios. Si el cliente se ajusta en esta categoría, llame a la función API [ScInitMapiUtil](scinitmapiutil.md) en lugar de la función [MAPIInitialize](mapiinitialize.md) en tiempo de inicialización. 
  
 **ScInitMapiUtil** permite a los clientes usar las funciones de utilidad que requieren asignadores de MAPI, pero que no le solicita a los asignadores de forma explícita. Cuando es el momento de apagar, llame a [DeinitMapiUtil](deinitmapiutil.md) para liberar recursos en lugar de [MAPIUninitialize](mapiuninitialize.md). Los clientes que no llaman nunca **MAPIInitialize** no deben llamar a **MAPIUninitialize**.
  
Si se ha llamado **ScInitMapiUtil** en lugar de **MAPIInitialize** y usan tablas a través de los métodos de **ITableData** en lugar de a través de los métodos **IMAPITable** , tenga en cuenta que no funcionarán las notificaciones de tabla. Las notificaciones requieren el uso de las bibliotecas de MAPI y [IMAPITable: IUnknown](imapitableiunknown.md).
  

