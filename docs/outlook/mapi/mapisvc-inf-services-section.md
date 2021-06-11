---
title: Sección MapiSvc.inf [Servicios]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434784"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="b1095-103">Sección MapiSvc.inf [Servicios]</span><span class="sxs-lookup"><span data-stu-id="b1095-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="b1095-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1095-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1095-105">La **sección [Servicios]** enumera los servicios de mensajes instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="b1095-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="b1095-106">Las entradas de esta sección usan el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="b1095-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="b1095-107">**[Servicios]**</span><span class="sxs-lookup"><span data-stu-id="b1095-107">**[Services]**</span></span>
  
 <span data-ttu-id="b1095-108">_nombre de la sección message-service_  =   _nombre del servicio de mensajes_</span><span class="sxs-lookup"><span data-stu-id="b1095-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="b1095-109">El nombre de la sección de servicio de mensajes es una cadena definida por el servicio de mensajes que vincula esta entrada a una sección correspondiente para el servicio en otro lugar de mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="b1095-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="b1095-110">El nombre del servicio de mensajes es el nombre del servicio instalado.</span><span class="sxs-lookup"><span data-stu-id="b1095-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="b1095-111">En la siguiente sección se muestran tres servicios de mensajes: la Libreta de direcciones predeterminada, Mi propio servicio y el servicio de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b1095-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="b1095-112">Estos servicios son ficticios, solo con fines ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="b1095-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="b1095-113">Cada implementador de servicio de mensajes sustituiría la entrada adecuada para su servicio de mensajes en esta sección.</span><span class="sxs-lookup"><span data-stu-id="b1095-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="b1095-114">Cada entrada de esta sección tiene una sección correspondiente en la que se almacena la información del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b1095-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="b1095-115">Por ejemplo, la sección correspondiente de la libreta de direcciones predeterminada se denomina [AB].</span><span class="sxs-lookup"><span data-stu-id="b1095-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

