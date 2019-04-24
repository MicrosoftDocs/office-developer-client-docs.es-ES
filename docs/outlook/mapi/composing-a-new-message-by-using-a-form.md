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
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335129"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Redactar un mensaje nuevo con un formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para usar un formulario para redactar un nuevo mensaje, primero debe crear un nuevo objeto de mensaje personalizado.
  
 **Para redactar un mensaje nuevo con un formulario**
  
1. Llame al método [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) del administrador de formularios para recuperar un puntero a un objeto de información de formulario (un objeto que implementa la interfaz [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) . 
    
2. Pase el puntero al objeto de información del formulario en una llamada a [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md). **CreateForm** carga el servidor de formularios apropiado. Además, pase un identificador de interfaz a **CreateForm** para especificar la interfaz que se va a usar para obtener acceso al nuevo mensaje. Normalmente, se solicita [IPersistMessage: IUnknown](ipersistmessageiunknown.md) pasando IID_IPersistMessage a **CreateForm**.
    
3. Guarde el nuevo mensaje llamando a su método [IPersistMessage:: Save](ipersistmessage-save.md) . El servidor de formularios debe establecer los valores de las propiedades requeridas del mensaje al crear el mensaje. 
    
4. Cargue el mensaje con una de estas dos estrategias: [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) o [IMAPISession::P Repareform](imapisession-prepareform.md) seguida de [IMAPISession:: ShowForm](imapisession-showform.md). Para obtener más información acerca de estas estrategias, consulte [cargar un mensaje en un formulario](loading-a-message-into-a-form.md).
    
> [!NOTE]
> Existen oportunidades para mejorar el rendimiento cuando se carga un nuevo mensaje personalizado en un servidor de formularios porque ya se ha tenido la oportunidad de obtener información sobre el mensaje (por ejemplo, su clase de mensaje) durante el procesamiento necesario para el ** **Llamadas a ResolveMessageClass y **CreateForm** . Por este motivo, podrá simplificar el procesamiento necesario antes de llamar a **LoadForm** sobre lo que se describe en el tema [cargar un mensaje en un formulario](loading-a-message-into-a-form.md). 
  

