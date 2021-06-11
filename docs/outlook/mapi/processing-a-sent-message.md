---
title: Procesamiento de un mensaje enviado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434679"
---
# <a name="processing-a-sent-message"></a>Procesamiento de un mensaje enviado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los mensajes salientes, una vez enviados, se pueden dejar en la carpeta Bandeja de salida, mover a una carpeta designada para contener los mensajes enviados o eliminarse. El tipo de procesamiento depende de si ha establecido o no las propiedades del almacén de mensajes:
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** es una propiedad booleana, establecida en TRUE si los mensajes deben eliminarse después de que se envíen y FALSE en caso contrario. **PR_SENTMAIL_ENTRYID** es el identificador de entrada de una carpeta. Cuando se establece esta propiedad, debe mover los mensajes enviados a la carpeta representada por este identificador de entrada. Los mensajes guardados normalmente tienen la identidad del último almacén de mensajes o proveedor de transporte para enviarlos. 
  
Una u otra, o ninguna de estas propiedades debe establecerse, pero no ambas. Sin embargo, si establece **PR_SENTMAIL_ENTRYID**, debe contener un identificador de entrada válido. 
  
En la tabla siguiente se describe cómo afectan estas propiedades a lo que se hace con los mensajes enviados.
  
|||
|:-----|:-----|
|Si no se establece ninguna propiedad:  <br/> |Deje el mensaje en la carpeta desde la que se envió (normalmente, la Bandeja de salida).  <br/> |
|Si **PR_SENTMAIL_ENTRYID** está establecido:  <br/> |Mueva el mensaje a la carpeta indicada.  <br/> |
|Si **PR_DELETE_AFTER_SUBMIT** está establecido:  <br/> |Elimine el mensaje.  <br/> |
   

