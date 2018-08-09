---
title: Procesar un mensaje enviado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0cea1a1008ecbff698b757d6c67af5c279954656
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820431"
---
# <a name="processing-a-sent-message"></a>Procesar un mensaje enviado

  
  
**Hace referencia a**: Outlook 
  
Salida de los mensajes, después de que se han enviado, puede dejarse en la Bandeja de salida carpeta, movido a una carpeta designada para almacenar los mensajes enviados o eliminado. El tipo de procesamiento depende de si se han establecido propiedades de almacén del mensaje:
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** es una propiedad booleana, establezca en TRUE si se deben eliminar los mensajes después de que se envían y FALSE en caso contrario. **PR_SENTMAIL_ENTRYID** es el identificador de entrada de una carpeta. Cuando se establece esta propiedad, debe mover los mensajes enviados a la carpeta representada por este identificador de entrada. Los mensajes guardados normalmente tienen la identidad del almacén de mensajes última o proveedor enviarlos de transporte. 
  
Debe ser uno o el otro o ninguna de estas propiedades set, pero no ambos. Sin embargo, si establece **PR_SENTMAIL_ENTRYID**, debe contener un identificador de entrada válido. 
  
En la siguiente tabla se describe cómo estas propiedades afectan a qué hacer con los mensajes enviados.
  
|||
|:-----|:-----|
|Si se establece ninguna de estas propiedades:  <br/> |Dejar el mensaje en la carpeta desde la que se envió (normalmente, la Bandeja de salida).  <br/> |
|Si se establece **PR_SENTMAIL_ENTRYID** :  <br/> |Mover el mensaje a la carpeta indicada.  <br/> |
|Si se establece **PR_DELETE_AFTER_SUBMIT** :  <br/> |Eliminar el mensaje.  <br/> |
   

