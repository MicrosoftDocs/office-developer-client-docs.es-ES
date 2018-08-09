---
title: Correlación TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Última modificación: 12 de marzo de 2013'
ms.openlocfilehash: b8b30dcc2fcf0c8e75004e36b6fd9f4f4583e304
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820868"
---
# <a name="tnef-correlation"></a><span data-ttu-id="e5d69-103">Correlación TNEF</span><span class="sxs-lookup"><span data-stu-id="e5d69-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="e5d69-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5d69-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5d69-105">Algunos sistemas de mensajería realizan una comprobación de correlación en cualquier secuencia de formato de encapsulación neutro para el transporte (TNEF) que se adjunta a un mensaje entrante para comprobar que la secuencia TNEF en realidad pertenecen a ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="e5d69-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="e5d69-106">Esto implica que coincidan con el valor de algún campo en el encabezado del mensaje entrante con una copia de ese valor almacenado en alguna propiedad en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="e5d69-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="e5d69-107">Los valores que son supuestamente únicos para cada mensaje, como los números de identificador de mensaje, se suelen usar para esto.</span><span class="sxs-lookup"><span data-stu-id="e5d69-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="e5d69-108">El transporte o la puerta de enlace que se creó la secuencia TNEF es responsable de elegir un valor apropiado en el encabezado del mensaje y coloca una copia en una propiedad adecuada antes de la codificación de propiedades de los mensajes salientes en la secuencia de TNEF.</span><span class="sxs-lookup"><span data-stu-id="e5d69-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="e5d69-109">Las puertas de enlace o los transportes que reciben el mensaje, a continuación, pueden extraer dicha propiedad de la secuencia TNEF y compruebe que su valor coincide con el valor del campo de encabezado correspondiente en el mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="e5d69-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="e5d69-110">Si los valores no coinciden, la puerta de enlace o transporte debe descartar la secuencia TNEF y proceso sólo el sobre del mensaje nativo.</span><span class="sxs-lookup"><span data-stu-id="e5d69-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="e5d69-111">Estos controles son prudentes debido a que los clientes de correo basado en MAPI no pueden adjuntar un archivo que contiene una secuencia de TNEF de los mensajes antiguos a una transferencia o incluso un mensaje sin relacionar; Si no está activado, este tipo de error puede causar la pérdida de texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e5d69-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="e5d69-112">El valor del campo de encabezado elegido debe ser único para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e5d69-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="e5d69-113">No hay ningún campo de encabezado fija para todos los sistemas de mensajería debido a que los sistemas de mensajería distintos usar los campos de encabezado diferentes, pero normalmente, el sistema de mensajería asigna un identificador único para el mensaje que es adecuado para este propósito.</span><span class="sxs-lookup"><span data-stu-id="e5d69-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="e5d69-114">Por ejemplo, sistemas de SMTP normalmente utilizan el encabezado MessageID, mientras sistemas X.400 normalmente usa el atributo IM_THIS_IPM.</span><span class="sxs-lookup"><span data-stu-id="e5d69-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

