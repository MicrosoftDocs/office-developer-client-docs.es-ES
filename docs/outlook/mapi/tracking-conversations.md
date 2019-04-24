---
title: Conversaciones de seguimiento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: 'Última modificación: 23 de julio de 2011'
localization_priority: Priority
ms.openlocfilehash: 3a59a7a15b4647832634adc4757544876b8841b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349549"
---
# <a name="tracking-conversations"></a><span data-ttu-id="91d84-103">Seguimiento de conversaciones</span><span class="sxs-lookup"><span data-stu-id="91d84-103">Tracking Conversations</span></span>

  
  
<span data-ttu-id="91d84-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91d84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91d84-p101">El seguimiento de conversaciones consiste en recopilar las respuestas a un mensaje. Los clientes deben establecer dos propiedades que ayudan a realizar el seguimiento de las conversaciones:</span><span class="sxs-lookup"><span data-stu-id="91d84-p101">Conversation tracking is collecting responses to a message. Clients should set two properties that aid in tracking conversations:</span></span>
  
- <span data-ttu-id="91d84-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="91d84-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span></span>
    
    <span data-ttu-id="91d84-108">**PR_CONVERSATION_TOPIC** es el asunto del mensaje normalizado, es decir, el asunto sin las cadenas de prefijos.</span><span class="sxs-lookup"><span data-stu-id="91d84-108">**PR_CONVERSATION_TOPIC** is the normalized subject of the message, the subject without the prefix strings.</span></span> <span data-ttu-id="91d84-109">Establezca esta propiedad con el valor de la propiedad **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="91d84-109">Set this property to the value of the message's **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> 
    
- <span data-ttu-id="91d84-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="91d84-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span></span>
    
    <span data-ttu-id="91d84-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span><span class="sxs-lookup"><span data-stu-id="91d84-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span></span> 
    
 <span data-ttu-id="91d84-p104">**ScCreateConversationIndex** genera el valor de un �ndice de conversaci�n para los mensajes salientes. **ScCreateConversationIndex** implementa el �ndice como un bloque de encabezado es 22 bytes de longitud, seguido de cero o m�s secundarios bloquean cada 5 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="91d84-p104">**ScCreateConversationIndex** generates the value of a conversation index for any outgoing message. **ScCreateConversationIndex** implements the index as a header block that is 22 bytes in length, followed by zero or more child blocks each 5 bytes in length.</span></span> 
  
<span data-ttu-id="91d84-116">El bloque de encabezado consta de 22 bytes, divididas en tres partes:</span><span class="sxs-lookup"><span data-stu-id="91d84-116">The header block is composed of 22 bytes, divided into three parts:</span></span>
  
- <span data-ttu-id="91d84-p105">Un byte reservado. Su valor es 1.</span><span class="sxs-lookup"><span data-stu-id="91d84-p105">One reserved byte. Its value is 1.</span></span>
    
- <span data-ttu-id="91d84-119">Cinco bytes para la hora del sistema actual se convierte en el formato de estructura [FILETIME](filetime.md) .</span><span class="sxs-lookup"><span data-stu-id="91d84-119">Five bytes for the current system time converted to the [FILETIME](filetime.md) structure format.</span></span> 
    
- <span data-ttu-id="91d84-120">Diecis�is bytes que contiene un [GUID](guid.md)o identificador �nico global.</span><span class="sxs-lookup"><span data-stu-id="91d84-120">Sixteen bytes holding a [GUID](guid.md), or globally unique identifier.</span></span>
    
<span data-ttu-id="91d84-121">Cada bloque secundarios se compone de 5 bytes, divididas como sigue:</span><span class="sxs-lookup"><span data-stu-id="91d84-121">Each child block is composed of 5 bytes, divided as follows:</span></span>
  
- <span data-ttu-id="91d84-p106">Un bit que contiene un c�digo que representa la diferencia entre la hora actual y el tiempo que se almacenan en el bloque de encabezado. Este bit ser� 0 si la diferencia es menor que.02 segundo y mayor de dos a�os y 1 si la diferencia es inferior a un segundo y mayor 56 a�os.</span><span class="sxs-lookup"><span data-stu-id="91d84-p106">One bit containing a code representing the difference between the current time and the time stored in the header block. This bit will be 0 if the difference is less than .02 second and greater than two years and 1 if the difference is less than one second and greater than 56 years.</span></span>
    
- <span data-ttu-id="91d84-p107">Bits de treinta uno que contiene la diferencia entre la hora actual y la hora en el bloque de encabezado expresada en unidades de **FILETIME**. Esta parte del bloque de secundarios se crearon con uno de dos estrategias, seg�n el valor del primer bit. Si este bit es cero, **ScCreateConversationIndex** descarta los bits superiores de 15 y 18 bits bajos. Si este bit es uno, la funci�n descarta los 10 bits alta y los 23 bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="91d84-p107">Thirty one bits containing the difference between the current time and the time in the header block expressed in **FILETIME** units.This part of the child block is produced using one of two strategies, depending on the value of the first bit. If this bit is zero, **ScCreateConversationIndex** discards the high 15 bits and the low 18 bits. If this bit is one, the function discards the high 10 bits and the low 23 bits.</span></span> 
    
- <span data-ttu-id="91d84-127">Cuatro bits que contiene un n�mero aleatorio generado por llamar a la funci�n de Win32 [GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="91d84-127">Four bits containing a random number generated by calling the Win32 function [GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).</span></span>
    
- <span data-ttu-id="91d84-128">Cuatro bits que contiene un recuento de secuencia que se obtiene de la parte del n�mero aleatorio.</span><span class="sxs-lookup"><span data-stu-id="91d84-128">Four bits containing a sequence count that is taken from part of the random number.</span></span>
    
<span data-ttu-id="91d84-129">Si decide establecer manualmente los �ndices de conversaci�n de mensajes, tenga en cuenta las siguientes sugerencias:</span><span class="sxs-lookup"><span data-stu-id="91d84-129">If you choose to set the conversation indexes of messages manually, consider the following suggestions:</span></span>
  
1. <span data-ttu-id="91d84-130">Mantener las diferencias en las zonas horarias de la contestan transparente; usar horas UTC en lugar de hora local.</span><span class="sxs-lookup"><span data-stu-id="91d84-130">Keep differences in the respondents' time zones transparent; use UTC times rather than local time.</span></span>
    
2. <span data-ttu-id="91d84-131">Aplicar sangr�a a cada grupo de conversaci�n en la misma cantidad.</span><span class="sxs-lookup"><span data-stu-id="91d84-131">Indent each conversation group by the same amount.</span></span>
    
3. <span data-ttu-id="91d84-132">Ordenar las respuestas a la misma fecha de mensaje.</span><span class="sxs-lookup"><span data-stu-id="91d84-132">Sort responses to the same message date.</span></span>
    
4. <span data-ttu-id="91d84-133">Subprocesos independientes iniciaron en momentos distintos que comparten el mismo tema.</span><span class="sxs-lookup"><span data-stu-id="91d84-133">Separate threads started at different times that happen to share the same topic.</span></span> 
    
5. <span data-ttu-id="91d84-134">Para implementar un orden categorizado, de forma tal que los mensajes se agrupen por tema, ordene por **PR_CONVERSATION_TOPIC** primero y luego por **PR_CONVERSATION_INDEX**.</span><span class="sxs-lookup"><span data-stu-id="91d84-134">To implement a categorized sort so that messages are grouped by topic, sort by **PR_CONVERSATION_TOPIC** first and then by **PR_CONVERSATION_INDEX**.</span></span> <span data-ttu-id="91d84-135">Para presentar los resultados de la ordenación, establezca la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) en 0 para los mensajes con un índice de conversación de 22 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="91d84-135">To present the results of the sort, set the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property to 0 for messages with a conversation index that is 22 bytes in length.</span></span> <span data-ttu-id="91d84-136">A continuación, para cada incremento de 5 bytes de longitud, aumente el valor de la propiedad **PR_DEPTH** en uno.</span><span class="sxs-lookup"><span data-stu-id="91d84-136">Then, for every 5-byte increment in the length, increment the value of the **PR_DEPTH** property by one.</span></span> 
    
<span data-ttu-id="91d84-137">El grupo PR_ORIGINAL de propiedades tambi�n puede utilizarse para realizar un seguimiento de conversaci�n.</span><span class="sxs-lookup"><span data-stu-id="91d84-137">The PR_ORIGINAL group of properties can also be used for conversation tracking.</span></span> <span data-ttu-id="91d84-138">Establecer estas propiedades para vincular responder o mensajes reenviados al mensaje original.</span><span class="sxs-lookup"><span data-stu-id="91d84-138">Set these properties to link reply or forwarded messages to the original message.</span></span> <span data-ttu-id="91d84-139">Todas las propiedades PR_ORIGINAL son opcionales.</span><span class="sxs-lookup"><span data-stu-id="91d84-139">All of the PR_ORIGINAL properties are optional.</span></span> <span data-ttu-id="91d84-140">Si no establece explícitamente, por ejemplo, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), el proveedor de almacenamiento de mensajes puede usar el valor predeterminado o el valor de la propiedad **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="91d84-140">If you do not explicitly set, for example, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), the message store provider can use the default value, or the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="91d84-141">De igual forma, si no establece **PR_ORIGINAL_AUTHOR_NAME** o **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), estas propiedades pueden establecer los valores predeterminados de las propiedades **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) y **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="91d84-141">Likewise, if you do not set **PR_ORIGINAL_AUTHOR_NAME** or **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), these properties can default to the values of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) properties, respectively.</span></span> 
  

