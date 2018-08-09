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
ms.openlocfilehash: 29a135264772847a624e1a4558b68bcf822b18df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816611"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="413a3-103">Crear un perfil con el Asistente de perfiles</span><span class="sxs-lookup"><span data-stu-id="413a3-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="413a3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="413a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="413a3-105">El Asistente para perfiles es una característica MAPI que permite a un usuario crear un perfil de la manera más sencilla posible.</span><span class="sxs-lookup"><span data-stu-id="413a3-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="413a3-106">El Asistente para perfiles, se muestra una serie de cuadros de diálogo que solicite al usuario que seleccione los servicios de mensajes y escriba los valores para algunas de las propiedades de configuración más esenciales.</span><span class="sxs-lookup"><span data-stu-id="413a3-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="413a3-107">Para la mayoría de las demás propiedades necesarias, el Asistente para perfiles utiliza los valores predeterminados proporcionados.</span><span class="sxs-lookup"><span data-stu-id="413a3-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="413a3-108">Para invocar al Asistente para perfiles, llamar a **LaunchWizard**, una función según el prototipo [LAUNCHWIZARDENTRY](launchwizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="413a3-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="413a3-109">El usuario puede agregar sólo los servicios de mensaje y los proveedores de servicios para el nuevo perfil que admiten al Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="413a3-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="413a3-110">Debido a que cada servicio de mensajes es posible que requieren que se establezcan que puede controlar el Asistente para perfiles más propiedades, tenga en cuenta que si utiliza este enfoque, es posible que uno o varios de los servicios seleccionados o proveedores a no esté completamente configurado.</span><span class="sxs-lookup"><span data-stu-id="413a3-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

