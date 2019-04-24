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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327401"
---
# <a name="tnef-correlation"></a><span data-ttu-id="4ed40-103">Correlación TNEF</span><span class="sxs-lookup"><span data-stu-id="4ed40-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="4ed40-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ed40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ed40-105">Algunos sistemas de mensajería realizan una comprobación de correlación en cualquier secuencia de formato de encapsulación neutro para el transporte (TNEF) que se adjunta a un mensaje entrante para comprobar que el flujo TNEF realmente pertenece a ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ed40-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="4ed40-106">Esto implica que se hace coincidir el valor de un campo en el encabezado del mensaje entrante con una copia de ese valor almacenada en alguna propiedad del flujo TNEF.</span><span class="sxs-lookup"><span data-stu-id="4ed40-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="4ed40-107">Para esto, se suelen usar valores que son únicos para cada mensaje, como los números de identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ed40-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="4ed40-108">El transporte o la puerta de enlace que creó la secuencia TNEF es responsable de elegir un valor apropiado del encabezado del mensaje y colocar una copia en una propiedad adecuada antes de codificar las propiedades del mensaje saliente en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="4ed40-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="4ed40-109">Las puertas de enlace o los transportes que reciben el mensaje pueden extraer la propiedad de la secuencia TNEF y comprobar que su valor coincida con el valor del campo de encabezado correspondiente en el mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="4ed40-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="4ed40-110">Si los valores no coinciden, la puerta de enlace o el transporte deben descartar la secuencia TNEF y procesar sólo el sobre del mensaje nativo.</span><span class="sxs-lookup"><span data-stu-id="4ed40-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="4ed40-111">Estas comprobaciones son prudentes porque los clientes de correo no basados en MAPI pueden adjuntar un archivo que contenga un flujo TNEF de un mensaje antiguo a un reenvío o incluso a un mensaje no relacionado; Si no se activa, un error de este tipo puede provocar la pérdida de texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ed40-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="4ed40-112">El valor del campo de encabezado elegido debe ser único para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ed40-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="4ed40-113">No hay ningún campo de encabezado fijo para todos los sistemas de mensajería, ya que los distintos sistemas de mensajería utilizan distintos campos de encabezado, pero normalmente el sistema de mensajería asigna un identificador único al mensaje que es adecuado para este propósito.</span><span class="sxs-lookup"><span data-stu-id="4ed40-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="4ed40-114">Por ejemplo, los sistemas SMTP usan normalmente el encabezado MessageID, mientras que los sistemas X. 400 normalmente usan el atributo IM_THIS_IPM.</span><span class="sxs-lookup"><span data-stu-id="4ed40-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

