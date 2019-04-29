---
title: Creación de un perfil con el Asistente para perfiles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a93cfb05d8abfffc9f55a7ea48efc3c3451dddbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411739"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Creación de un perfil con el Asistente para perfiles

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El Asistente para perfiles es una característica MAPI que permite a un usuario crear un perfil de la forma más sencilla posible. El Asistente para perfiles muestra una serie de cuadros de diálogo que solicitan al usuario que seleccione servicios de mensajes y escriben valores para algunas de las propiedades de configuración más esenciales. Para la mayoría de las demás propiedades necesarias, el Asistente para perfiles usa los valores predeterminados proporcionados. Para invocar al Asistente para perfiles, llame a **LaunchWizard**, una función basada en el prototipo [LAUNCHWIZARDENTRY](launchwizardentry.md) . 
  
El usuario solo puede Agregar los servicios de mensajes y proveedores de servicios al nuevo perfil que admite el Asistente para perfiles. Dado que cada servicio de mensajes puede requerir que se establezcan más propiedades de las que el Asistente para perfiles puede controlar, tenga en cuenta que si usa este enfoque, es posible que uno o más servicios o proveedores seleccionados se configuren de forma incompleta.
  

