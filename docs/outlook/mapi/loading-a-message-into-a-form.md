---
title: Cargar un mensaje en un formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412418"
---
# <a name="loading-a-message-into-a-form"></a>Cargar un mensaje en un formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para cargar un mensaje existente en un formulario mediante un servidor de formularios, use una de las siguientes estrategias.
  
- Llame a [IMAPISession::P repareform](imapisession-prepareform.md) para crear un token y, a continuación, [IMAPISession:: ShowForm](imapisession-showform.md) para mostrar el formulario. 
    
- Llamar a [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md). 
    
El uso de la estrategia **PrepareForm** y **ShowForm** es comparativamente fácil, pero da como resultado formularios que son modales con respecto a su cliente. Esto se debe a que la llamada a **ShowForm** no devuelve ningún valor hasta que se haya salido del formulario. Si necesita controlar formularios de forma asincrónica, no use esta estrategia. 
  
El uso de la estrategia **LoadForm** es más difícil porque el método requiere varios parámetros. Estos parámetros indican al administrador de formularios que inicie el servidor de formularios apropiado en el contexto adecuado y muestre el mensaje correcto. Si el servidor de formularios ya se está ejecutando, el administrador de formularios carga el mensaje en el servidor de formularios sin iniciar una nueva instancia del servidor de formularios. 
  
Para especificar el servidor de formulario que se iniciará, pase la clase de mensaje controlada por el servidor de destino en el contenido del parámetro _lpszMessageClass_ . La clase de mensaje adecuada puede determinarse recuperando la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje que se va a cargar. A veces, no hay ningún servidor de formularios para la clase de mensaje especificada, sólo un servidor de formularios que controla mensajes pertenecientes a la superclase del mensaje. Si prefiere que el mensaje se cargue solo por un servidor de formularios específicamente diseñado para controlar los mensajes de esa clase, establezca la marca MAPIFORM_EXACTMATCH en la llamada **LoadForm** . Para obtener más información, consulte [clases de mensajes MAPI](mapi-message-classes.md).
  
 <b0>LoadForm</b0> también requiere un puntero al sitio de mensajes del visor y al contexto de la vista, y al valor de los <b1>PR_MSG_STATUS</b1> (<b2>PidTagMessageStatus</b2>) y <b3>PR_MESSAGE_FLAGS</b3> (<b4>PidTagMessageFlags</b4>) del mensaje de destino. </a1>.
  

