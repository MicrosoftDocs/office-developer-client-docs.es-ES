---
title: Mostrar iconos de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438634"
---
# <a name="displaying-form-icons"></a>Mostrar iconos de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al mostrar una lista de mensajes en una carpeta, resulta útil para los usuarios si distingue los mensajes con clases de mensajes personalizadas del IPM estándar. Nota de los mensajes. Las clases de mensajes personalizadas corresponden a servidores de formulario y los servidores de formulario proporcionan iconos para representarse a sí mismos. Puede mostrar estos iconos en la lista de mensajes para alertar a los usuarios de la clase de mensaje de cada mensaje antes de que el usuario abra los mensajes. Normalmente, el icono de la propiedad PR_MINI_ICON **(** [PidTagMiniIcon](pidtagminiicon-canonical-property.md)) del formulario es el que debe mostrarse en la lista de mensajes. Los formularios **también tienen una PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) que se puede mostrar cuando el formulario se minimiza en una hoja de propiedades.
  
 **Para obtener un icono para una clase de mensaje sin activar el servidor de formularios para esa clase de mensaje**
  
1. Llame al [método IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) para obtener un puntero a una [interfaz IMAPIFormContainer : IUnknown.](imapiformcontaineriunknown.md) 
    
2. Llama al [método IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) para obtener un puntero a una [interfaz IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md) 
    
3. Llama al [método IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) para obtener un identificador de icono. 
    
A continuación, el icono se puede mostrar con las API estándar de Win32.
  
> [!IMPORTANT]
> Una vez que tenga el icono para una clase de mensaje, haga todo lo posible para almacenar en caché ese icono. No almacenar en caché iconos afecta gravemente al rendimiento de las aplicaciones cliente. Al almacenar en caché iconos, tenga cuidado con las relaciones entre las clases de mensaje y sus subclases. Por ejemplo, si el IPM. La clase de mensaje Note.Meeting.Cancel vuelve a resolverse en IPM. Tenga en cuenta que no se supone que todas las subclases de IPM. Tenga en cuenta que debe usar el icono de IPM. Nota. 
  

