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
# <a name="tracking-conversations"></a>Conversaciones de seguimiento

  
  
**Se aplica a**: Outlook 
  
Conversaci�n de seguimiento est� recopilando las respuestas a un mensaje. Clientes deben establecer dos propiedades que facilitan el seguimiento de las conversaciones:
  
- **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** es el asunto del mensaje, el asunto sin las cadenas de prefijo normalizado. Establecer esta propiedad en el valor de la propiedad del mensaje **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)). 
    
- **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))
    
    **PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI. 
    
 **ScCreateConversationIndex** genera el valor de un �ndice de conversaci�n para los mensajes salientes. **ScCreateConversationIndex** implementa el �ndice como un bloque de encabezado es 22 bytes de longitud, seguido de cero o m�s secundarios bloquean cada 5 bytes de longitud. 
  
El bloque de encabezado consta de 22 bytes, divididas en tres partes:
  
- Un byte reservado. Su valor es 1.
    
- Cinco bytes para la hora del sistema actual se convierte en el formato de estructura [FILETIME](filetime.md) . 
    
- Diecis�is bytes que contiene un [GUID](guid.md)o identificador �nico global.
    
Cada bloque secundarios se compone de 5 bytes, divididas como sigue:
  
- Un bit que contiene un c�digo que representa la diferencia entre la hora actual y el tiempo que se almacenan en el bloque de encabezado. Este bit ser� 0 si la diferencia es menor que.02 segundo y mayor de dos a�os y 1 si la diferencia es inferior a un segundo y mayor 56 a�os.
    
- Bits de treinta uno que contiene la diferencia entre la hora actual y la hora en el bloque de encabezado expresada en unidades de **FILETIME**. Esta parte del bloque de secundarios se crearon con uno de dos estrategias, seg�n el valor del primer bit. Si este bit es cero, **ScCreateConversationIndex** descarta los bits superiores de 15 y 18 bits bajos. Si este bit es uno, la funci�n descarta los 10 bits alta y los 23 bits inferiores. 
    
- Cuatro bits que contiene un n�mero aleatorio generado por llamar a la funci�n de Win32 [GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx).
    
- Cuatro bits que contiene un recuento de secuencia que se obtiene de la parte del n�mero aleatorio.
    
Si decide establecer manualmente los �ndices de conversaci�n de mensajes, tenga en cuenta las siguientes sugerencias:
  
1. Mantener las diferencias en las zonas horarias de la contestan transparente; usar horas UTC en lugar de hora local.
    
2. Aplicar sangr�a a cada grupo de conversaci�n en la misma cantidad.
    
3. Ordenar las respuestas a la misma fecha de mensaje.
    
4. Subprocesos independientes iniciaron en momentos distintos que comparten el mismo tema. 
    
5. Para implementar a una ordenaci�n por categor�as para que los mensajes se agrupan por tema, ordenar por primera **PR_CONVERSATION_TOPIC** y a continuaci�n, **PR_CONVERSATION_INDEX**. Para presentar los resultados de la ordenación, establezca la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) en 0 para los mensajes con un índice de conversación es 22 bytes de longitud. A continuaci�n, para cada incremento de 5 bytes en la longitud, incrementar el valor de la propiedad **PR_DEPTH** en uno. 
    
El grupo PR_ORIGINAL de propiedades tambi�n puede utilizarse para realizar un seguimiento de conversaci�n. Establecer estas propiedades para vincular responder o mensajes reenviados al mensaje original. Todas las propiedades PR_ORIGINAL son opcionales. Si no establece explícitamente, por ejemplo, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), el proveedor de almacén de mensajes puede usar el valor predeterminado o el valor de la **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) propiedad. Del mismo modo, si no se establece **PR_ORIGINAL_AUTHOR_NAME** o **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), estas propiedades pueden de forma predeterminada en los valores de la **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) y **PR_ CLIENT_SUBMIT_TIME** propiedades ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)), respectivamente. 
  

