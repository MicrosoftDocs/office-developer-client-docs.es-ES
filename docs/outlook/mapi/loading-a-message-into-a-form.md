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
  
- Llame a [IMAPISession::P repareForm](imapisession-prepareform.md) para crear un token y, a continuación, [IMAPISession::ShowForm](imapisession-showform.md) para mostrar el formulario. 
    
- Llame [a IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md). 
    
El uso **de la estrategia PrepareForm** y **ShowForm** es relativamente fácil, pero da como resultado formularios que son modales con respecto al cliente. Esto se debe a que la llamada **a ShowForm** no vuelve hasta que se cierra el formulario. Si necesita controlar los formularios de forma asincrónica, no use esta estrategia. 
  
El uso **de la estrategia LoadForm** es más difícil porque el método requiere varios parámetros. Estos parámetros instruyen al administrador de formularios que inicie el servidor de formulario adecuado en el contexto adecuado y muestre el mensaje adecuado. Si el servidor de formularios ya se está ejecutando, el administrador de formularios carga el mensaje en el servidor de formularios sin iniciar una nueva instancia del servidor de formularios. 
  
Para especificar el servidor de formulario que se va a iniciar, pase la clase de mensaje que controla el servidor de destino en el contenido del parámetro _lpszMessageClass._ La clase de mensaje adecuada se puede determinar recuperando la **propiedad PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje que se va a cargar. A veces no hay ningún servidor de formulario para la clase de mensaje especificada, solo un servidor de formulario que controla los mensajes que pertenecen a la superclase del mensaje. Si prefiere que el mensaje solo lo cargue un servidor de formularios diseñado específicamente para controlar los mensajes de esa clase, establezca la marca MAPIFORM_EXACTMATCH en la **llamada LoadForm.** Para obtener más información, vea [clases de mensajes MAPI](mapi-message-classes.md).
  
 **LoadForm** también requiere un puntero al sitio de mensajes y al contexto de vista del visor, así como el valor de las propiedades **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) y **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje de destino.
  

