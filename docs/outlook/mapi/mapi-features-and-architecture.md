---
title: Arquitectura y características de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 34bae703-a979-437c-9d86-8b91e9822a54
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8156cb53fc81f4861e4a66da4960df0458ec6c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418284"
---
# <a name="mapi-features-and-architecture"></a><span data-ttu-id="a1122-103">Arquitectura y características de MAPI</span><span class="sxs-lookup"><span data-stu-id="a1122-103">MAPI Features and Architecture</span></span>

  
  
<span data-ttu-id="a1122-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1122-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1122-105">La API de mensajería (MAPI) se compone de un conjunto de interfaces de programación de aplicaciones comunes y un componente de biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="a1122-105">Messaging API (MAPI) is composed of a set of common application programming interfaces and a dynamic-link library (DLL) component.</span></span> <span data-ttu-id="a1122-106">Las interfaces se usan para crear y tener acceso a diferentes aplicaciones de mensajería y sistemas de mensajería, lo que ofrece un entorno uniforme para el desarrollo y el uso, y proporciona auténtica independencia para ambos.</span><span class="sxs-lookup"><span data-stu-id="a1122-106">The interfaces are used to create and access diverse messaging applications and messaging systems, offering a uniform environment for development and use, and providing true independence for both.</span></span> <span data-ttu-id="a1122-107">La DLL contiene el subsistema MAPI, que administra la interacción entre las aplicaciones de mensajería front-end y los sistemas de mensajería back-end, y proporciona una interfaz de usuario común para las tareas frecuentes.</span><span class="sxs-lookup"><span data-stu-id="a1122-107">The DLL contains the MAPI subsystem, which manages the interaction between front-end messaging applications and back-end messaging systems and provides a common user interface for frequent tasks.</span></span> <span data-ttu-id="a1122-108">El subsistema MAPI actúa como un centro de activación central para unificar los distintos sistemas de mensajería y proteger a los clientes de sus diferencias.</span><span class="sxs-lookup"><span data-stu-id="a1122-108">The MAPI subsystem acts as a central clearinghouse to unify the various messaging systems and shield clients from their differences.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a1122-109">Ver también</span><span class="sxs-lookup"><span data-stu-id="a1122-109">See also</span></span>



[<span data-ttu-id="a1122-110">Conceptos de MAPI</span><span class="sxs-lookup"><span data-stu-id="a1122-110">MAPI Concepts</span></span>](mapi-concepts.md)

