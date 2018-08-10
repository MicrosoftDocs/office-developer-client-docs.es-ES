---
title: Compatibilidad con texto con formato Representaci�n de los datos adjuntos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68abe85b-5dc0-40d0-8917-30ea002aa816
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 14c1162bd4e225fd3ab2ea5ab11536b3bdf08edd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820786"
---
# <a name="supporting-formatted-text-rendering-attachments"></a>Compatibilidad con texto con formato: Representaci�n de los datos adjuntos

  
  
**Hace referencia a**: Outlook 
  
Una aplicación cliente que se importan a donde se representan sus datos adjuntos en un mensaje, Establece la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para estos datos adjuntos durante la composición de mensaje. Un cliente que no necesita conocer la colocaci�n de representaci�n sale de esta propiedad no definidas.
  
Cuando un cliente, abre un mensaje con datos adjuntos, intenta recuperar la propiedad de **PR_RENDERING_POSITION** de cada documento adjunto para determinar donde se deben representar los datos adjuntos en el texto del mensaje. Un cliente puede usar uno de los m�todos siguientes para recuperar **PR_RENDERING_POSITION**:
  
- [IMAPIProp::GetProps](imapiprop-getprops.md) on the open attachment to retrieve the **PR_RENDERING_POSITION** property. 
    
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) on the open message to retrieve its attachment table. **PR_RENDERING_POSITION** is a required column in all attachment tables. This is the preferred method because it results in better performance. 
    
Los almacenes de mensajes RTF compatible pueden elegir si se debe devolver un valor preciso o aproximado para **PR_RENDERING_POSITION**. Dado que los almacenes de mensajes volver a calcular el valor de **PR_RENDERING_POSITION** de datos adjuntos cuando se le pida la propiedad del mensaje **PR_BODY**, algunos mensajes RTF cuenta almacena s�lo se establece la posici�n de la precisi�n de representaci�n cuando un cliente solicita primero **PR_BODY**garant�a. Se permiten los almacenes de mensajes RTF para proporcionar a los clientes con los valores de posici�n de representaci�n aproximada para mejorar el rendimiento. Proporcionar un aproximado en lugar de una posici�n de representaci�n precisa ahorra tiempo y es suficiente para la mayor�a de las situaciones. 
  
Los almacenes de mensajes RTF cuenta deben basar su aproximaci�n en el valor especificado por el cliente responsable de la creaci�n de los datos adjuntos. Aunque todos los clientes deben establecer **PR_RENDERING_POSITION**, los proveedores de almac�n de mensajes deben estar preparados para abordar los problemas con la posibilidad de que su ausencia. Cuando el cliente no establece **PR_RENDERING_POSITION**, un almac�n de mensajes puede establecer a -1 para indicar que la posici�n de representaci�n no est� comprendido en el texto del mensaje. En cualquier lugar dentro del mensaje seg�n el cliente se pueden mostrar los datos adjuntos con una posici�n de representaci�n de -1. Muchos clientes colocar estos tipos de datos adjuntos en la parte superior del mensaje.
  
El grado de precisión de una propiedad **PR_RENDERING_POSITION** depende de si un almacén de mensajes guarda tanto un mensaje **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) y las propiedades **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o sólo **PR_RTF_COMPRESSED**. Si el cliente genera **PR_BODY** y guarda en el almac�n de mensajes junto con el texto con formato, las posiciones de representaci�n ser� precisas. Sin embargo, si el almac�n de mensajes debe generar su propia versi�n del **PR_BODY** porque s�lo guarda **PR_RTF_COMPRESSED**, es probable que las posiciones de representaci�n algo imprecisos. Esto es debido a las diferencias en la forma en que los clientes y los proveedores de almac�n de mensajes generan la propiedad **PR_BODY**. 
  
To calculate an accurate **PR_RENDERING_POSITION** value, an RTF-aware store uses a tag embedded in the formatted text. The utility function **RTFSync** can be called to perform this calculation and update an attachment's rendering position. Depending on the amount of state information available, the message store can pass either RTF_SYNC_BODY_CHANGED, RTF_SYNC_RTF_CHANGED, or both values to [RTFSync](rtfsync.md).
  

