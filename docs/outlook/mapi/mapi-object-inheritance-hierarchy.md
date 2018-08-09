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
ms.openlocfilehash: a03b994a613bbb1f17db3e3220b7e053989c278a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818152"
---
# <a name="mapi-object-inheritance-hierarchy"></a>Jerarquía de herencia de objetos MAPI

**Hace referencia a**: Outlook 
  
Todas las interfaces implementadas por objetos MAPI se heredan de [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), la interfaz OLE que permite a los objetos para comunicarse. La mayoría de las interfaces heredan directamente de **IUnknown**, pero algunas heredan de una de las otras dos interfaces bases: [IMAPIProp: IUnknown](imapipropiunknown.md) o [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). En la siguiente ilustración muestra la jerarquía de herencia completa de MAPI.
  
**Jerarquía de herencia de MAPI**
  
![Jerarquía de herencia de MAPI] (media/amapi_06.gif "Jerarquía de herencia de MAPI")
  
## <a name="see-also"></a>Vea también

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Objeto MAPI e Introducción a la interfaz](mapi-object-and-interface-overview.md)

