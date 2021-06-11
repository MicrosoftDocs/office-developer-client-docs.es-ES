---
title: Redacción de un nuevo mensaje mediante un formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412803"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Redacción de un nuevo mensaje mediante un formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para usar un formulario para redactar un nuevo mensaje, cree primero un nuevo objeto de mensaje personalizado.
  
 **Para redactar un nuevo mensaje con un formulario**
  
1. Llame al método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) del administrador de formularios para recuperar un puntero a un objeto de información de formulario, un objeto que implementa la interfaz [IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md) 
    
2. Pase el puntero al objeto de información del formulario en una llamada a [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm** carga el servidor de formulario adecuado. Además, pase un identificador de interfaz a **CreateForm** para especificar la interfaz que se usará para obtener acceso al nuevo mensaje. Normalmente, se solicita [IPersistMessage : IUnknown](ipersistmessageiunknown.md) pasando IID_IPersistMessage a **CreateForm**.
    
3. Guarde el nuevo mensaje llamando a su [método IPersistMessage::Save.](ipersistmessage-save.md) El servidor de formularios debe establecer valores para las propiedades necesarias del mensaje cuando cree el mensaje. 
    
4. Cargue el mensaje mediante una de dos estrategias: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) o [IMAPISession::P repareForm](imapisession-prepareform.md) seguido de [IMAPISession::ShowForm](imapisession-showform.md). Para obtener más información acerca de estas estrategias, vea [Loading a Message Into a Form](loading-a-message-into-a-form.md).
    
> [!NOTE]
> Existen oportunidades para obtener mejoras en el rendimiento al cargar un nuevo mensaje personalizado en un servidor de formularios porque ya habrá tenido la oportunidad de obtener información sobre el mensaje , como su clase de mensaje, durante el procesamiento necesario para las llamadas **ResolveMessageClass** y **CreateForm.** Debido a esto, podrá simplificar el procesamiento necesario antes de llamar [a](loading-a-message-into-a-form.md) **LoadForm** sobre lo descrito en el tema Loading a Message Into a Form . 
  

