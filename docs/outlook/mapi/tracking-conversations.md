---
title: Conversaciones de seguimiento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 58157d597d3bb1042d6bc16ff954495a507c8333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820883"
---
# <a name="tracking-conversations"></a><span data-ttu-id="378d5-103">Conversaciones de seguimiento</span><span class="sxs-lookup"><span data-stu-id="378d5-103">Tracking Conversations</span></span>

  
  
<span data-ttu-id="378d5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="378d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="378d5-p101">Conversaci�n de seguimiento est� recopilando las respuestas a un mensaje. Clientes deben establecer dos propiedades que facilitan el seguimiento de las conversaciones:</span><span class="sxs-lookup"><span data-stu-id="378d5-p101">Conversation tracking is collecting responses to a message. Clients should set two properties that aid in tracking conversations:</span></span>
  
- <span data-ttu-id="378d5-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="378d5-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span></span>
    
    <span data-ttu-id="378d5-108">**PR_CONVERSATION_TOPIC** es el asunto del mensaje, el asunto sin las cadenas de prefijo normalizado.</span><span class="sxs-lookup"><span data-stu-id="378d5-108">**PR_CONVERSATION_TOPIC** is the normalized subject of the message, the subject without the prefix strings.</span></span> <span data-ttu-id="378d5-109">Establecer esta propiedad en el valor de la propiedad del mensaje **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="378d5-109">Set this property to the value of the message's **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> 
    
- <span data-ttu-id="378d5-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="378d5-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span></span>
    
    <span data-ttu-id="378d5-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span><span class="sxs-lookup"><span data-stu-id="378d5-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span></span> 
    
 <span data-ttu-id="378d5-p104">**ScCreateConversationIndex** genera el valor de un �ndice de conversaci�n para los mensajes salientes. **ScCreateConversationIndex** implementa el �ndice como un bloque de encabezado es 22 bytes de longitud, seguido de cero o m�s secundarios bloquean cada 5 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="378d5-p104">**ScCreateConversationIndex** generates the value of a conversation index for any outgoing message. **ScCreateConversationIndex** implements the index as a header block that is 22 bytes in length, followed by zero or more child blocks each 5 bytes in length.</span></span> 
  
<span data-ttu-id="378d5-116">El bloque de encabezado consta de 22 bytes, divididas en tres partes:</span><span class="sxs-lookup"><span data-stu-id="378d5-116">The header block is composed of 22 bytes, divided into three parts:</span></span>
  
- <span data-ttu-id="378d5-p105">Un byte reservado. Su valor es 1.</span><span class="sxs-lookup"><span data-stu-id="378d5-p105">One reserved byte. Its value is 1.</span></span>
    
- <span data-ttu-id="378d5-119">Cinco bytes para la hora del sistema actual se convierte en el formato de estructura [FILETIME](filetime.md) .</span><span class="sxs-lookup"><span data-stu-id="378d5-119">Five bytes for the current system time converted to the [FILETIME](filetime.md) structure format.</span></span> 
    
- <span data-ttu-id="378d5-120">Diecis�is bytes que contiene un [GUID](guid.md)o identificador �nico global.</span><span class="sxs-lookup"><span data-stu-id="378d5-120">Sixteen bytes holding a [GUID](guid.md), or globally unique identifier.</span></span>
    
<span data-ttu-id="378d5-121">Cada bloque secundarios se compone de 5 bytes, divididas como sigue:</span><span class="sxs-lookup"><span data-stu-id="378d5-121">Each child block is composed of 5 bytes, divided as follows:</span></span>
  
- <span data-ttu-id="378d5-p106">Un bit que contiene un c�digo que representa la diferencia entre la hora actual y el tiempo que se almacenan en el bloque de encabezado. Este bit ser� 0 si la diferencia es menor que.02 segundo y mayor de dos a�os y 1 si la diferencia es inferior a un segundo y mayor 56 a�os.</span><span class="sxs-lookup"><span data-stu-id="378d5-p106">One bit containing a code representing the difference between the current time and the time stored in the header block. This bit will be 0 if the difference is less than .02 second and greater than two years and 1 if the difference is less than one second and greater than 56 years.</span></span>
    
- <span data-ttu-id="378d5-p107">Bits de treinta uno que contiene la diferencia entre la hora actual y la hora en el bloque de encabezado expresada en unidades de **FILETIME**. Esta parte del bloque de secundarios se crearon con uno de dos estrategias, seg�n el valor del primer bit. Si este bit es cero, **ScCreateConversationIndex** descarta los bits superiores de 15 y 18 bits bajos. Si este bit es uno, la funci�n descarta los 10 bits alta y los 23 bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="378d5-p107">Thirty one bits containing the difference between the current time and the time in the header block expressed in **FILETIME** units.This part of the child block is produced using one of two strategies, depending on the value of the first bit. If this bit is zero, **ScCreateConversationIndex** discards the high 15 bits and the low 18 bits. If this bit is one, the function discards the high 10 bits and the low 23 bits.</span></span> 
    
- <span data-ttu-id="378d5-127">Cuatro bits que contiene un n�mero aleatorio generado por llamar a la funci�n de Win32 [GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="378d5-127">Four bits containing a random number generated by calling the Win32 function [GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx).</span></span>
    
- <span data-ttu-id="378d5-128">Cuatro bits que contiene un recuento de secuencia que se obtiene de la parte del n�mero aleatorio.</span><span class="sxs-lookup"><span data-stu-id="378d5-128">Four bits containing a sequence count that is taken from part of the random number.</span></span>
    
<span data-ttu-id="378d5-129">Si decide establecer manualmente los �ndices de conversaci�n de mensajes, tenga en cuenta las siguientes sugerencias:</span><span class="sxs-lookup"><span data-stu-id="378d5-129">If you choose to set the conversation indexes of messages manually, consider the following suggestions:</span></span>
  
1. <span data-ttu-id="378d5-130">Mantener las diferencias en las zonas horarias de la contestan transparente; usar horas UTC en lugar de hora local.</span><span class="sxs-lookup"><span data-stu-id="378d5-130">Keep differences in the respondents' time zones transparent; use UTC times rather than local time.</span></span>
    
2. <span data-ttu-id="378d5-131">Aplicar sangr�a a cada grupo de conversaci�n en la misma cantidad.</span><span class="sxs-lookup"><span data-stu-id="378d5-131">Indent each conversation group by the same amount.</span></span>
    
3. <span data-ttu-id="378d5-132">Ordenar las respuestas a la misma fecha de mensaje.</span><span class="sxs-lookup"><span data-stu-id="378d5-132">Sort responses to the same message date.</span></span>
    
4. <span data-ttu-id="378d5-133">Subprocesos independientes iniciaron en momentos distintos que comparten el mismo tema.</span><span class="sxs-lookup"><span data-stu-id="378d5-133">Separate threads started at different times that happen to share the same topic.</span></span> 
    
5. <span data-ttu-id="378d5-134">Para implementar a una ordenaci�n por categor�as para que los mensajes se agrupan por tema, ordenar por primera **PR_CONVERSATION_TOPIC** y a continuaci�n, **PR_CONVERSATION_INDEX**.</span><span class="sxs-lookup"><span data-stu-id="378d5-134">To implement a categorized sort so that messages are grouped by topic, sort by **PR_CONVERSATION_TOPIC** first and then by **PR_CONVERSATION_INDEX**.</span></span> <span data-ttu-id="378d5-135">Para presentar los resultados de la ordenación, establezca la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) en 0 para los mensajes con un índice de conversación es 22 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="378d5-135">To present the results of the sort, set the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property to 0 for messages with a conversation index that is 22 bytes in length.</span></span> <span data-ttu-id="378d5-136">A continuaci�n, para cada incremento de 5 bytes en la longitud, incrementar el valor de la propiedad **PR_DEPTH** en uno.</span><span class="sxs-lookup"><span data-stu-id="378d5-136">Then, for every 5-byte increment in the length, increment the value of the **PR_DEPTH** property by one.</span></span> 
    
<span data-ttu-id="378d5-137">El grupo PR_ORIGINAL de propiedades tambi�n puede utilizarse para realizar un seguimiento de conversaci�n.</span><span class="sxs-lookup"><span data-stu-id="378d5-137">The PR_ORIGINAL group of properties can also be used for conversation tracking.</span></span> <span data-ttu-id="378d5-138">Establecer estas propiedades para vincular responder o mensajes reenviados al mensaje original.</span><span class="sxs-lookup"><span data-stu-id="378d5-138">Set these properties to link reply or forwarded messages to the original message.</span></span> <span data-ttu-id="378d5-139">Todas las propiedades PR_ORIGINAL son opcionales.</span><span class="sxs-lookup"><span data-stu-id="378d5-139">All of the PR_ORIGINAL properties are optional.</span></span> <span data-ttu-id="378d5-140">Si no establece explícitamente, por ejemplo, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), el proveedor de almacén de mensajes puede usar el valor predeterminado o el valor de la **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) propiedad.</span><span class="sxs-lookup"><span data-stu-id="378d5-140">If you do not explicitly set, for example, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), the message store provider can use the default value, or the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="378d5-141">Del mismo modo, si no se establece **PR_ORIGINAL_AUTHOR_NAME** o **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), estas propiedades pueden de forma predeterminada en los valores de la **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) y **PR_ CLIENT_SUBMIT_TIME** propiedades ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="378d5-141">Likewise, if you do not set **PR_ORIGINAL_AUTHOR_NAME** or **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), these properties can default to the values of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) properties, respectively.</span></span> 
  

