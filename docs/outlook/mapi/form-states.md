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
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429169"
---
# <a name="form-states"></a><span data-ttu-id="53792-103">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="53792-103">Form states</span></span>

<span data-ttu-id="53792-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53792-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53792-105">Los objetos de formulario pueden estar en uno de cinco Estados distintos, en función de los métodos a los que se haya llamado y si se han producido errores en la realización de esos métodos.</span><span class="sxs-lookup"><span data-stu-id="53792-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="53792-106">Los Estados se describen en los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="53792-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="53792-107">Estado sin inicializar</span><span class="sxs-lookup"><span data-stu-id="53792-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="53792-108">Estado normal</span><span class="sxs-lookup"><span data-stu-id="53792-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="53792-109">Estado noScribble</span><span class="sxs-lookup"><span data-stu-id="53792-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="53792-110">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="53792-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="53792-111">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="53792-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="53792-112">Los Estados están principalmente relacionados con el estado de los datos del objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="53792-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="53792-113">Los diferentes Estados reflejan si es necesario guardar los datos, si el objeto de formulario debe permitir modificaciones a los datos y en qué punto del proceso se guardan los datos en el formulario.</span><span class="sxs-lookup"><span data-stu-id="53792-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="53792-114">Por lo tanto, los Estados de formulario y las transiciones entre ellos tienen más que ver con la implementación del servidor de formularios de [IPersistMessage:](ipersistmessageiunknown.md) métodos de interfaz IUnknown que otros.</span><span class="sxs-lookup"><span data-stu-id="53792-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="53792-115">Conocer estos Estados es muy útil para la correcta implementación de las interfaces de formulario MAPI que debe implementar su servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="53792-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="53792-116">En los temas de esta sección se describen los distintos Estados, junto con las acciones permitidas que provocan transiciones a otros Estados.</span><span class="sxs-lookup"><span data-stu-id="53792-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="53792-117">No se permiten las transiciones que no aparezcan en los temas.</span><span class="sxs-lookup"><span data-stu-id="53792-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="53792-118">Si los objetos de formulario realizan transiciones entre Estados no permitidos, no se comportarán de la manera que esperan los clientes de mensajería y podrían provocar un comportamiento impredecible del cliente o del objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="53792-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="53792-119">Algunas transiciones de estado dependen de la información de los Estados anteriores.</span><span class="sxs-lookup"><span data-stu-id="53792-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="53792-120">El servidor de formularios probablemente tendrá que implementar una marca en sus objetos de formulario para indicar si los valores de las propiedades del mensaje se han cambiado para facilitar los cambios de estado posteriores.</span><span class="sxs-lookup"><span data-stu-id="53792-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53792-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="53792-121">See also</span></span>

- [<span data-ttu-id="53792-122">Desarrollar servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="53792-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

