---
title: Muestra iconos de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b2e79e5568de38bee9a97c9df2598b30f1ba1bdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816694"
---
# <a name="displaying-form-icons"></a>Muestra iconos de formulario

  
  
**Hace referencia a**: Outlook 
  
Cuando se muestra una lista de mensajes en una carpeta, es útil para los usuarios distinguir los mensajes con clases de mensaje personalizadas desde el formulario estándar IPM. Tenga en cuenta los mensajes. Clases de mensaje personalizadas se corresponden con los servidores de formulario y los servidores de formulario proporcionan iconos para representar a sí mismos. Puede mostrar estos iconos en la lista de mensajes de alerta a los usuarios a la clase de mensaje de cada mensaje antes de que el usuario abre los mensajes. Normalmente, el icono de la propiedad del formulario **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) es el que deben mostrarse en la lista de mensajes. Formularios también tienen una propiedad de **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) que se puede mostrar cuando el formulario está minimizado en una hoja de propiedades.
  
 **Para obtener un icono para una clase de mensaje sin activar el servidor de formulario para esa clase de mensaje**
  
1. Llame al método [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) para obtener un puntero a un [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) interfaz. 
    
2. Llame al método [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) para obtener un puntero a un [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) interfaz. 
    
3. Llame al método [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) para obtener un identificador de icono. 
    
A continuación, se muestra el icono con la API de Win32 estándar.
  
> [!IMPORTANT]
> Una vez que el icono de una clase de mensaje, asegúrese de todos los esfuerzos para almacenar en caché ese icono. No almacenar en caché los iconos gravemente afecta al rendimiento de las aplicaciones cliente. Al almacenar en caché los iconos, tenga cuidado de las relaciones entre las clases de mensajes y sus subclases. Por ejemplo, si el formulario IPM. Clase de mensaje Note.Meeting.Cancel sucede resolver en IPM. Tenga en cuenta, no asuma que todas las subclases de IPM. Nota debe usar el icono para IPM. Tenga en cuenta. 
  

