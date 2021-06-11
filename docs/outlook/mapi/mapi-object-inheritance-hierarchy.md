---
title: Jerarquía de herencia de objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345846"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Jerarquía de herencia de objetos MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todas las interfaces implementadas por objetos MAPI heredan en última instancia de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), la interfaz OLE que permite que los objetos se comuniquen. La mayoría de las interfaces heredan directamente de **IUnknown,** pero algunas heredan de otras dos interfaces base: [IMAPIProp : IUnknown](imapipropiunknown.md) o [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). En la ilustración siguiente se muestra la jerarquía de herencia completa en MAPI.
  
**Jerarquía de herencia de MAPI**
  
![Jerarquía de herencia MAPI jerarquía]de herencia(media/amapi_06.gif "MAPI")
  
## <a name="see-also"></a>Vea también

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Introducción a la interfaz y el objeto MAPI](mapi-object-and-interface-overview.md)

