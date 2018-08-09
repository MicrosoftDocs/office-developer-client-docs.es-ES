---
title: Inicializar las herramientas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8ee0504d4a8b9e2ce96e42a53b778d4e3f518fcc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817818"
---
# <a name="initializing-the-mapi-utilities"></a>Inicializar las herramientas MAPI

  
  
**Hace referencia a**: Outlook 
  
Si la única parte de MAPI que necesita para usar son las utilidades, las interfaces y funciones declaran en MAPIUTIL de MAPI. Archivo de encabezado según se trate como **IPropData** y **ITableData** : no es necesario llamar a **MAPIInitialize** para la inicialización. Para obtener más información, vea [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)y [MAPIInitialize](mapiinitialize.md). En su lugar, llame a la función **ScInitMapiUtil** . Para obtener más información, vea [ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** permite que las aplicaciones de cliente usar las funciones de utilidad y métodos que requieren asignadores de MAPI, pero que no los pida explícitamente. 
  
Durante el apagado, realice una llamada a **DeinitMapiUtil** para liberar recursos conectados a las utilidades. No llame a **MAPIUninitialize**. Para obtener más información, vea [DeinitMapiUtil](deinitmapiutil.md) y [MAPIUninitialize](mapiuninitialize.md).
  
Tenga en cuenta que la interfaz de **ITableData** no admite las notificaciones de tabla para los clientes que se han llamado **ScInitMapiUtil** en lugar de **MAPIInitialize**. 
  

