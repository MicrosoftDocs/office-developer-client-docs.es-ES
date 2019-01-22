---
title: Seguimiento de conversaciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: 'Última modificación: 23 de julio de 2011'
localization_priority: Priority
ms.openlocfilehash: 3a59a7a15b4647832634adc4757544876b8841b1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706227"
---
# <a name="tracking-conversations"></a>Seguimiento de conversaciones

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
El seguimiento de conversaciones consiste en recopilar las respuestas a un mensaje. Los clientes deben establecer dos propiedades que ayudan a realizar el seguimiento de las conversaciones:
  
- **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** es el asunto del mensaje normalizado, es decir, el asunto sin las cadenas de prefijos. Establezca esta propiedad con el valor de la propiedad **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) del mensaje. 
    
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
    
- Cuatro bits que contiene un n�mero aleatorio generado por llamar a la funci�n de Win32 [GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).
    
- Cuatro bits que contiene un recuento de secuencia que se obtiene de la parte del n�mero aleatorio.
    
Si decide establecer manualmente los �ndices de conversaci�n de mensajes, tenga en cuenta las siguientes sugerencias:
  
1. Mantener las diferencias en las zonas horarias de la contestan transparente; usar horas UTC en lugar de hora local.
    
2. Aplicar sangr�a a cada grupo de conversaci�n en la misma cantidad.
    
3. Ordenar las respuestas a la misma fecha de mensaje.
    
4. Subprocesos independientes iniciaron en momentos distintos que comparten el mismo tema. 
    
5. Para implementar un orden categorizado, de forma tal que los mensajes se agrupen por tema, ordene por **PR_CONVERSATION_TOPIC** primero y luego por **PR_CONVERSATION_INDEX**. Para presentar los resultados de la ordenación, establezca la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) en 0 para los mensajes con un índice de conversación de 22 bytes de longitud. A continuación, para cada incremento de 5 bytes de longitud, aumente el valor de la propiedad **PR_DEPTH** en uno. 
    
El grupo PR_ORIGINAL de propiedades tambi�n puede utilizarse para realizar un seguimiento de conversaci�n. Establecer estas propiedades para vincular responder o mensajes reenviados al mensaje original. Todas las propiedades PR_ORIGINAL son opcionales. Si no establece explícitamente, por ejemplo, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), el proveedor de almacenamiento de mensajes puede usar el valor predeterminado o el valor de la propiedad **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). De igual forma, si no establece **PR_ORIGINAL_AUTHOR_NAME** o **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), estas propiedades pueden establecer los valores predeterminados de las propiedades **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) y **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)), respectivamente. 
  

