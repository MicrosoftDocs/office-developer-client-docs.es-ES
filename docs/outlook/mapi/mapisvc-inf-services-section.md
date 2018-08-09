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
ms.openlocfilehash: 19031f6c02f3e8e925adfc8d2affa43fb6532fee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818285"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="33c46-103">Sección MapiSvc.inf [Servicios]</span><span class="sxs-lookup"><span data-stu-id="33c46-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="33c46-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33c46-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33c46-105">La sección **[Services]** enumera los servicios de mensaje que se instalan en un equipo.</span><span class="sxs-lookup"><span data-stu-id="33c46-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="33c46-106">Las entradas de esta sección use el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="33c46-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="33c46-107">**[Services]**</span><span class="sxs-lookup"><span data-stu-id="33c46-107">**[Services]**</span></span>
  
 <span data-ttu-id="33c46-108">_nombre de la sección servicio de mensajes_ =  _nombre de servicio de mensajes_</span><span class="sxs-lookup"><span data-stu-id="33c46-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="33c46-109">El nombre de la sección servicio de mensajes es que una cadena definida por el servicio de mensajes que se vincula esta entrada a una sección correspondiente para el servicio en el resto de mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="33c46-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="33c46-110">El nombre de servicio de mensajes es el nombre del servicio instalado.</span><span class="sxs-lookup"><span data-stu-id="33c46-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="33c46-111">En la sección siguiente se muestra tres servicios de mensaje: la libreta de direcciones predeterminada, mi propio servicio y el servicio de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="33c46-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="33c46-112">Estos servicios son ficticios, únicamente con fines de ilustración.</span><span class="sxs-lookup"><span data-stu-id="33c46-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="33c46-113">Cada implementador del servicio mensaje sería sustituir la entrada adecuada para su servicio de mensajes en esta sección.</span><span class="sxs-lookup"><span data-stu-id="33c46-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="33c46-114">Cada entrada de esta sección tiene una sección correspondiente de su propio donde se almacena la información para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="33c46-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="33c46-115">Por ejemplo, la sección correspondiente de la libreta de direcciones predeterminada se denomina [AB].</span><span class="sxs-lookup"><span data-stu-id="33c46-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

