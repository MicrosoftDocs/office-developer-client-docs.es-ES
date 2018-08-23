---
title: Estados de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 195a82bfcc163ee01d2d42c71e79a8f5c9c620e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564636"
---
# <a name="form-states"></a><span data-ttu-id="bece6-103">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="bece6-103">Form states</span></span>

<span data-ttu-id="bece6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bece6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bece6-105">Objetos de formulario pueden estar en uno de cinco estados distintos, dependiendo de qué se ha llamado a los métodos en ellos y si los errores se han producido en la realización de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bece6-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="bece6-106">Los Estados se describen en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="bece6-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="bece6-107">Estado sin inicializar</span><span class="sxs-lookup"><span data-stu-id="bece6-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="bece6-108">Estado normal</span><span class="sxs-lookup"><span data-stu-id="bece6-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="bece6-109">Estado NoScribble</span><span class="sxs-lookup"><span data-stu-id="bece6-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="bece6-110">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="bece6-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="bece6-111">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="bece6-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="bece6-112">Los Estados principalmente se relacionan con el estado de los datos en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="bece6-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="bece6-113">Los distintos Estados reflejan si los datos se deben guardar, si el objeto de formulario debe permitir que las modificaciones realizadas en los datos y qué punto en el proceso de guardar los datos que el formulario está en.</span><span class="sxs-lookup"><span data-stu-id="bece6-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="bece6-114">Por lo tanto, el formulario Estados y transiciones entre ellas tienen mucho más relacionada con la implementación del servidor de su formulario de [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos que cualquier otro de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="bece6-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="bece6-115">Conocimiento de estos Estados es muy útil para la correcta ejecución de las interfaces de formulario MAPI que debe implementar el servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="bece6-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="bece6-116">En los temas de esta sección se describen los distintos Estados, junto con las acciones permitidas que causar transiciones a otros Estados.</span><span class="sxs-lookup"><span data-stu-id="bece6-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="bece6-117">No se permiten las transiciones no aparece en los temas.</span><span class="sxs-lookup"><span data-stu-id="bece6-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="bece6-118">Si los objetos de formulario realizar transiciones no permitidas entre Estados, no se comportará de las maneras en que los clientes de mensajería esperan y podrían causar un comportamiento inesperado objeto cliente o formulario.</span><span class="sxs-lookup"><span data-stu-id="bece6-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bece6-119">Algunas transiciones de estado dependen de la información de estados anteriores.</span><span class="sxs-lookup"><span data-stu-id="bece6-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="bece6-120">El servidor de formulario muy probable que deba implementar un indicador en sus objetos de formulario para indicar si han cambiado los valores de las propiedades del mensaje para facilitar los cambios de estado de una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="bece6-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bece6-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="bece6-121">See also</span></span>

- [<span data-ttu-id="bece6-122">Desarrollar servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="bece6-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

