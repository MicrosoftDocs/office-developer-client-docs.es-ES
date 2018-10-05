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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391790"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Jerarquía de herencia de objetos MAPI

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Todas las interfaces implementadas por objetos MAPI se heredan de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), la interfaz OLE que permite a los objetos para comunicarse. La mayoría de las interfaces heredan directamente de **IUnknown**, pero algunas heredan de una de las otras dos interfaces bases: [IMAPIProp: IUnknown](imapipropiunknown.md) o [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). En la siguiente ilustración muestra la jerarquía de herencia completa de MAPI.
  
**Jerarquía de herencia de MAPI**
  
![Jerarquía de herencia de MAPI] (media/amapi_06.gif "Jerarquía de herencia de MAPI")
  
## <a name="see-also"></a>Vea también

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Objeto MAPI e Introducción a la interfaz](mapi-object-and-interface-overview.md)

