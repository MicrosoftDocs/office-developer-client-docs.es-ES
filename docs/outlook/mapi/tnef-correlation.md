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
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410374"
---
# <a name="tnef-correlation"></a><span data-ttu-id="c555d-103">Correlación TNEF</span><span class="sxs-lookup"><span data-stu-id="c555d-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="c555d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c555d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c555d-105">Algunos sistemas de mensajería realizan una comprobación de correlación en cualquier secuencia de formato de encapsulamiento de Transport-Neutral (TNEF) adjunta a un mensaje entrante para comprobar que la secuencia TNEF pertenece de hecho a ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="c555d-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="c555d-106">Esto implica hacer coincidir el valor de algún campo en el encabezado del mensaje entrante con una copia de ese valor almacenada en alguna propiedad de la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="c555d-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="c555d-107">Normalmente se usan valores que son presumiblemente únicos para cada mensaje, como los números de id. de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c555d-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="c555d-108">El transporte o la puerta de enlace que creó la secuencia TNEF es responsable de elegir un valor adecuado del encabezado del mensaje y colocar una copia en una propiedad adecuada antes de codificar las propiedades del mensaje saliente en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="c555d-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="c555d-109">Las puertas de enlace o los transportes que reciben el mensaje pueden extraer esa propiedad de la secuencia TNEF y comprobar que su valor coincide con el valor del campo de encabezado correspondiente en el mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="c555d-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="c555d-110">Si los valores no coinciden, la puerta de enlace o el transporte deben descartar la secuencia TNEF y procesar solo el sobre del mensaje nativo.</span><span class="sxs-lookup"><span data-stu-id="c555d-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="c555d-111">Estas comprobaciones son prudentes porque los clientes de correo no basados en MAPI pueden adjuntar un archivo que contiene una secuencia TNEF de un mensaje antiguo a un reenvío o incluso un mensaje no relacionado; si no se comprueba, este error puede provocar la pérdida del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c555d-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="c555d-112">El valor del campo de encabezado elegido debe ser único para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c555d-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="c555d-113">No hay ningún campo de encabezado fijo para todos los sistemas de mensajería porque diferentes sistemas de mensajería usan campos de encabezado diferentes, pero normalmente el sistema de mensajería asigna un identificador único al mensaje que es adecuado para este propósito.</span><span class="sxs-lookup"><span data-stu-id="c555d-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="c555d-114">Por ejemplo, los sistemas SMTP suelen usar el encabezado MessageID, mientras que los sistemas X.400 suelen usar el IM_THIS_IPM principal.</span><span class="sxs-lookup"><span data-stu-id="c555d-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

