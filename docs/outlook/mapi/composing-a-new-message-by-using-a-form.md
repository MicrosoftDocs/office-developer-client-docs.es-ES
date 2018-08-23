---
title: Redactar un mensaje nuevo con un formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 667d7afe1772786507ffc8eb75f901439ada61d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587872"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Redactar un mensaje nuevo con un formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para usar un formulario para redactar un mensaje nuevo, en primer lugar hay que crear un nuevo objeto de mensaje personalizado.
  
 **Para redactar un nuevo mensaje mediante un formulario**
  
1. Llamar al método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) del director de formulario para recuperar un puntero a un objeto de información de un formulario, un objeto que implementa el [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) interfaz. 
    
2. Pase el puntero al objeto de información de formulario en una llamada a [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm** carga el servidor de forma adecuada. Además, puede pasar un identificador de interfaz a **CreateForm** para especificar la interfaz que se usará para tener acceso al mensaje nuevo. Normalmente, se solicita [IPersistMessage: IUnknown](ipersistmessageiunknown.md) pasando IID_IPersistMessage al **CreateForm**.
    
3. Guarde el nuevo mensaje mediante una llamada a su método [IPersistMessage::Save](ipersistmessage-save.md) . El servidor de formulario debe establecer los valores de las propiedades del mensaje necesarios cuando crea el mensaje. 
    
4. Cargar el mensaje mediante uno de dos estrategias: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) o [IMAPISession:: PrepareForm](imapisession-prepareform.md) seguido [IMAPISession:: ShowForm](imapisession-showform.md). Para obtener más información acerca de estas estrategias, vea [cargar un mensaje en un formulario](loading-a-message-into-a-form.md).
    
> [!NOTE]
> Existen oportunidades de ganancias en el rendimiento al cargar un nuevo mensaje personalizado en un servidor de formulario porque ya habrá tenía una oportunidad para obtener información acerca del mensaje, como su clase de mensaje: durante el procesamiento necesario para la ** ResolveMessageClass** y **CreateForm** llamadas. Por este motivo, podrá simplificar el procesamiento necesario antes de llamar a **LoadForm** a través de la se describe en el tema [al cargar un mensaje en un formulario](loading-a-message-into-a-form.md). 
  

