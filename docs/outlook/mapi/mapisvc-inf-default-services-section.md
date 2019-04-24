---
title: Sección MapiSvc. inf [servicios preDeterminados]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270073"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="eca58-103">Sección MapiSvc. inf [servicios preDeterminados]</span><span class="sxs-lookup"><span data-stu-id="eca58-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="eca58-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eca58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eca58-105">La sección **[default Services]** muestra todos los servicios de mensajes que están seleccionados como los servicios de mensajes predeterminados.</span><span class="sxs-lookup"><span data-stu-id="eca58-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="eca58-106">Estos servicios de mensajes predeterminados son un subconjunto de los servicios de mensajes que se enumeran en la sección **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="eca58-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="eca58-107">Cuando un programa de configuración de perfiles crea un perfil predeterminado, los servicios de mensajes de esta sección se incluyen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="eca58-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="eca58-108">Las entradas usan el mismo formato que las entradas de la sección **[Services]** , como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="eca58-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="eca58-109">**[Servicios preDeterminados]**</span><span class="sxs-lookup"><span data-stu-id="eca58-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="eca58-110">_nombre de sección de servicio de mensajes_ =  _nombre del servicio de mensajes_</span><span class="sxs-lookup"><span data-stu-id="eca58-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="eca58-111">Las siguientes entradas se incluirán en la sección **[default Services]** del archivo MAPISVC. inf que se muestra en la ilustración anterior:</span><span class="sxs-lookup"><span data-stu-id="eca58-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


