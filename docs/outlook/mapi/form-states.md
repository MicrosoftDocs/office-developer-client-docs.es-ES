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
# <a name="form-states"></a><span data-ttu-id="82493-103">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="82493-103">Form states</span></span>

<span data-ttu-id="82493-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82493-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82493-105">Los objetos form pueden encontrarse en uno de los cinco estados distintos, en función de los métodos que se hayan llamado en ellos y de si se han producido errores al realizar dichos métodos.</span><span class="sxs-lookup"><span data-stu-id="82493-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="82493-106">Los estados se describen en los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="82493-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="82493-107">Estado no inicializado</span><span class="sxs-lookup"><span data-stu-id="82493-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="82493-108">Estado normal</span><span class="sxs-lookup"><span data-stu-id="82493-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="82493-109">Estado nocribible</span><span class="sxs-lookup"><span data-stu-id="82493-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="82493-110">Estado de HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="82493-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="82493-111">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="82493-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="82493-112">Los estados se relacionan principalmente con el estado de los datos en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="82493-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="82493-113">Los distintos estados reflejan si los datos deben guardarse, si el objeto de formulario debe permitir modificaciones en los datos y en qué punto del proceso de guardar los datos en los que se encuentra el formulario.</span><span class="sxs-lookup"><span data-stu-id="82493-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="82493-114">Por lo tanto, los estados de formulario y las transiciones entre ellos tienen más que ver con la implementación del servidor de formulario de los métodos de interfaz [IPersistMessage : IUnknown](ipersistmessageiunknown.md) que cualquier otro.</span><span class="sxs-lookup"><span data-stu-id="82493-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="82493-115">El conocimiento de estos estados es muy útil para la correcta implementación de las interfaces de formulario MAPI que debe implementar el servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="82493-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="82493-116">En los temas de esta sección se describen los distintos estados, junto con las acciones permitidas que provocan transiciones a otros estados.</span><span class="sxs-lookup"><span data-stu-id="82493-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="82493-117">No se permiten las transiciones que no aparecen en los temas.</span><span class="sxs-lookup"><span data-stu-id="82493-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="82493-118">Si los objetos de formulario hacen transiciones no permitidos entre estados, no se comportarán de la manera que los clientes de mensajería esperan y podrían provocar un comportamiento impredecible del cliente o del objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="82493-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="82493-119">Algunas transiciones de estado dependen de la información de estados anteriores.</span><span class="sxs-lookup"><span data-stu-id="82493-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="82493-120">Lo más probable es que el servidor de formulario tenga que implementar una marca en sus objetos de formulario para indicar si los valores de las propiedades del mensaje se han cambiado para facilitar cambios de estado posteriores.</span><span class="sxs-lookup"><span data-stu-id="82493-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82493-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="82493-121">See also</span></span>

- [<span data-ttu-id="82493-122">Desarrollo de servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="82493-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

