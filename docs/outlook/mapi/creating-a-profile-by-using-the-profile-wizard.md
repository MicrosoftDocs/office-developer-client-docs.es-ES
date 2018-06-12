---
title: Creación de un perfil mediante el Asistente para perfiles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 29a135264772847a624e1a4558b68bcf822b18df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816611"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Creación de un perfil mediante el Asistente para perfiles

  
  
**Se aplica a**: Outlook 
  
El Asistente para perfiles es una característica MAPI que permite a un usuario crear un perfil de la manera más sencilla posible. El Asistente para perfiles, se muestra una serie de cuadros de diálogo que solicite al usuario que seleccione los servicios de mensajes y escriba los valores para algunas de las propiedades de configuración más esenciales. Para la mayoría de las demás propiedades necesarias, el Asistente para perfiles utiliza los valores predeterminados proporcionados. Para invocar al Asistente para perfiles, llamar a **LaunchWizard**, una función según el prototipo [LAUNCHWIZARDENTRY](launchwizardentry.md) . 
  
El usuario puede agregar sólo los servicios de mensaje y los proveedores de servicios para el nuevo perfil que admiten al Asistente para perfiles. Debido a que cada servicio de mensajes es posible que requieren que se establezcan que puede controlar el Asistente para perfiles más propiedades, tenga en cuenta que si utiliza este enfoque, es posible que uno o varios de los servicios seleccionados o proveedores a no esté completamente configurado.
  

