---
title: Inicialización de las utilidades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420951"
---
# <a name="initializing-the-mapi-utilities"></a>Inicialización de las utilidades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si la única parte de MAPI que necesita usar son las utilidades, las interfaces y funciones declaradas en MAPIUTIL de MAPI. Archivo de encabezado H como **IPropData** e **ITableData:** no es necesario llamar a **MAPIInitialize** para la inicialización. Para obtener más información, vea [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md)y [MAPIInitialize](mapiinitialize.md). En su lugar, llame a **la función ScInitMapiUtil.** Para obtener más información, [vea ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** permite a las aplicaciones cliente usar funciones de utilidad y métodos que requieren asignadores MAPI, pero que no las solicitan explícitamente. 
  
En el momento del cierre, realice una llamada a **DeinitMapiUtil para** liberar recursos conectados a las utilidades. No llame a **MAPIUninitialize**. Para obtener más información, vea [DeinitMapiUtil](deinitmapiutil.md) y [MAPIUninitialize](mapiuninitialize.md).
  
Tenga en cuenta que la **interfaz ITableData** no admite notificaciones de tabla para clientes que han llamado **a ScInitMapiUtil en** lugar de **MAPIInitialize**. 
  

