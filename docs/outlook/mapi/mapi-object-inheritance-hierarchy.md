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
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="165fa-103">Jerarquía de herencia de objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="165fa-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="165fa-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="165fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="165fa-105">Todas las interfaces implementadas por objetos MAPI se heredan de [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), la interfaz OLE que permite a los objetos para comunicarse.</span><span class="sxs-lookup"><span data-stu-id="165fa-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="165fa-106">La mayoría de las interfaces heredan directamente de **IUnknown**, pero algunas heredan de una de las otras dos interfaces bases: [IMAPIProp: IUnknown](imapipropiunknown.md) o [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="165fa-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="165fa-107">En la siguiente ilustración muestra la jerarquía de herencia completa de MAPI.</span><span class="sxs-lookup"><span data-stu-id="165fa-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="165fa-108">**Jerarquía de herencia de MAPI**</span><span class="sxs-lookup"><span data-stu-id="165fa-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="165fa-109">![Jerarquía de herencia de MAPI] (media/amapi_06.gif "Jerarquía de herencia de MAPI")</span><span class="sxs-lookup"><span data-stu-id="165fa-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="165fa-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="165fa-110">See also</span></span>

- [<span data-ttu-id="165fa-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="165fa-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="165fa-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="165fa-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="165fa-113">Objeto MAPI e Introducción a la interfaz</span><span class="sxs-lookup"><span data-stu-id="165fa-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

