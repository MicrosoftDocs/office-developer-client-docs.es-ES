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
ms.openlocfilehash: d677958b1a429201c05b5195c58bd7462d0f3d37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818031"
---
# <a name="loading-a-message-into-a-form"></a>Cargar un mensaje en un formulario

  
  
**Hace referencia a**: Outlook 
  
Para cargar un mensaje existente en un formulario mediante un servidor de formulario, utilice una de las siguientes estrategias.
  
- [IMAPISession:: PrepareForm](imapisession-prepareform.md) para crear un token de llamadas y, a continuación, [IMAPISession:: ShowForm](imapisession-showform.md) para mostrar el formulario. 
    
- Llame a [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md). 
    
Uso de la estrategia de **PrepareForm** y **ShowForm** es tan fácil, pero da como resultado de los formularios que son modales con respecto a su cliente. Esto es debido a que la llamada a **ShowForm** no devuelve hasta que haya salido el formulario. Si necesita administrar formularios de forma asincrónica, no use esta estrategia. 
  
Uso de la estrategia de **LoadForm** es más difícil debido a que el método requiere varios parámetros. Estos parámetros instruir al administrador de formulario para iniciar el servidor de formulario correcto en el contexto adecuado y mostrar el mensaje adecuado. Si ya se está ejecutando el servidor de formulario, el Administrador de formularios de carga el mensaje en el servidor de formulario sin necesidad de iniciar una nueva instancia del servidor de formulario. 
  
Para especificar qué servidor de formulario para iniciar, pase la clase de mensaje controlada por el servidor de destino en el contenido del parámetro _lpszMessageClass_ . La clase de mensaje adecuado se puede determinar mediante la recuperación de la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje que se va a cargar. En ocasiones, no hay ningún servidor de formulario para la clase de mensaje especificado, sólo el servidor de un formulario administra los mensajes que pertenecen a la superclase del mensaje. Si prefiere que el mensaje se puede cargar sólo por un servidor de formulario diseñado específicamente para administrar los mensajes de esa clase, establezca el indicador MAPIFORM_EXACTMATCH en la llamada **LoadForm** . Para obtener más información, vea [Las clases de mensajes de MAPI](mapi-message-classes.md).
  
 **LoadForm** también requiere un puntero al sitio de mensaje del su visor y contexto de vista y el valor para el mensaje de destino **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) y **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) Propiedades.
  

