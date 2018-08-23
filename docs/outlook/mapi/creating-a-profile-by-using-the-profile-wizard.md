---
title: Crear un perfil con el Asistente de perfiles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f30dca8323f74bc2817bab375b58fcc1bc15c18b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574261"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="23433-103">Crear un perfil con el Asistente de perfiles</span><span class="sxs-lookup"><span data-stu-id="23433-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="23433-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23433-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23433-105">El Asistente para perfiles es una característica MAPI que permite a un usuario crear un perfil de la manera más sencilla posible.</span><span class="sxs-lookup"><span data-stu-id="23433-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="23433-106">El Asistente para perfiles, se muestra una serie de cuadros de diálogo que solicite al usuario que seleccione los servicios de mensajes y escriba los valores para algunas de las propiedades de configuración más esenciales.</span><span class="sxs-lookup"><span data-stu-id="23433-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="23433-107">Para la mayoría de las demás propiedades necesarias, el Asistente para perfiles utiliza los valores predeterminados proporcionados.</span><span class="sxs-lookup"><span data-stu-id="23433-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="23433-108">Para invocar al Asistente para perfiles, llamar a **LaunchWizard**, una función según el prototipo [LAUNCHWIZARDENTRY](launchwizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="23433-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="23433-109">El usuario puede agregar sólo los servicios de mensaje y los proveedores de servicios para el nuevo perfil que admiten al Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="23433-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="23433-110">Debido a que cada servicio de mensajes es posible que requieren que se establezcan que puede controlar el Asistente para perfiles más propiedades, tenga en cuenta que si utiliza este enfoque, es posible que uno o varios de los servicios seleccionados o proveedores a no esté completamente configurado.</span><span class="sxs-lookup"><span data-stu-id="23433-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

