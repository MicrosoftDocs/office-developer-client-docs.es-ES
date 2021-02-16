---
title: Creación de un perfil mediante el Asistente para perfiles
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
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="a6b95-103">Creación de un perfil mediante el Asistente para perfiles</span><span class="sxs-lookup"><span data-stu-id="a6b95-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="a6b95-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6b95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6b95-105">El Asistente para perfiles es una característica MAPI que permite al usuario crear un perfil de la forma más sencilla posible.</span><span class="sxs-lookup"><span data-stu-id="a6b95-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="a6b95-106">El Asistente para perfiles muestra una serie de cuadros de diálogo que solicitan al usuario que seleccione los servicios de mensajes y escriba valores para algunas de las propiedades de configuración más esenciales.</span><span class="sxs-lookup"><span data-stu-id="a6b95-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="a6b95-107">Para la mayoría de las demás propiedades necesarias, el Asistente para perfiles usa los valores predeterminados proporcionados.</span><span class="sxs-lookup"><span data-stu-id="a6b95-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="a6b95-108">Para invocar el Asistente para perfiles, llame a **LaunchWizard**, una función basada en el prototipo [LAUNCHWIZARDENTRY.](launchwizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="a6b95-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="a6b95-109">El usuario solo puede agregar los servicios de mensajes y los proveedores de servicios al nuevo perfil que admiten el Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="a6b95-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="a6b95-110">Dado que cada servicio de mensajes puede requerir establecer más propiedades de las que puede controlar el Asistente para perfiles, tenga en cuenta que si usa este enfoque, es posible que uno o varios de los servicios o proveedores seleccionados estén configurados de forma incompleta.</span><span class="sxs-lookup"><span data-stu-id="a6b95-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

