---
title: Sección MapiSvc.inf [Servicios predeterminados]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573148"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="011c6-103">Sección MapiSvc.inf [Servicios predeterminados]</span><span class="sxs-lookup"><span data-stu-id="011c6-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="011c6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="011c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="011c6-105">La sección **[Services predeterminado]** enumera todos los servicios de mensaje que se han seleccionado como servicios de mensajes de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="011c6-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="011c6-106">Estos servicios de mensaje predeterminada son un subconjunto de los servicios de mensaje que aparecen en la sección **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="011c6-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="011c6-107">Cuando un programa de configuración de perfil crea un perfil de forma predeterminada, los servicios de mensaje en esta sección se incluyen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="011c6-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="011c6-108">Las entradas de utilizan el mismo formato como entradas de la sección **[Services]** , como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="011c6-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="011c6-109">**[Servicios predeterminados]**</span><span class="sxs-lookup"><span data-stu-id="011c6-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="011c6-110">_nombre de la sección servicio de mensajes_ =  _nombre de servicio de mensajes_</span><span class="sxs-lookup"><span data-stu-id="011c6-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="011c6-111">Las siguientes entradas se incluirá en la sección **[Services predeterminado]** para el mapisvc.inf que se muestra en la ilustración anterior:</span><span class="sxs-lookup"><span data-stu-id="011c6-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


