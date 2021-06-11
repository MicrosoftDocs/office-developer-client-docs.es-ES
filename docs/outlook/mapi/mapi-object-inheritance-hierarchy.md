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
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="d4012-103">Jerarquía de herencia de objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="d4012-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="d4012-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4012-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4012-105">Todas las interfaces implementadas por objetos MAPI heredan en última instancia de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), la interfaz OLE que permite que los objetos se comuniquen.</span><span class="sxs-lookup"><span data-stu-id="d4012-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="d4012-106">La mayoría de las interfaces heredan directamente de **IUnknown,** pero algunas heredan de otras dos interfaces base: [IMAPIProp : IUnknown](imapipropiunknown.md) o [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="d4012-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="d4012-107">En la ilustración siguiente se muestra la jerarquía de herencia completa en MAPI.</span><span class="sxs-lookup"><span data-stu-id="d4012-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="d4012-108">**Jerarquía de herencia de MAPI**</span><span class="sxs-lookup"><span data-stu-id="d4012-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="d4012-109">![Jerarquía de herencia MAPI jerarquía]de herencia(media/amapi_06.gif "MAPI")</span><span class="sxs-lookup"><span data-stu-id="d4012-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d4012-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4012-110">See also</span></span>

- [<span data-ttu-id="d4012-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4012-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="d4012-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d4012-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="d4012-113">Introducción a la interfaz y el objeto MAPI</span><span class="sxs-lookup"><span data-stu-id="d4012-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

