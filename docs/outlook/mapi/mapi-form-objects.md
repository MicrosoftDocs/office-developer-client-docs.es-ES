---
title: Objetos de formulario MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5a7c6c575f277a91a18f0d834e26d3d376613fba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404788"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="4d694-103">Objetos de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="4d694-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="4d694-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d694-105">Los servidores de formulario crean dinámicamente objetos de formulario para mostrar mensajes específicos y permitir a los usuarios interactuar con ellos.</span><span class="sxs-lookup"><span data-stu-id="4d694-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="4d694-106">Por lo tanto, un objeto de formulario es una instancia de la clase derivada de [IMAPIForm](imapiformiunknown.md) que implementa el servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="4d694-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="4d694-107">Cuando una aplicación cliente abre un mensaje, el servidor de formulario de esa clase de mensaje crea un objeto de formulario para controlar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4d694-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="4d694-108">A continuación, el objeto form crea su interfaz y muestra las propiedades del mensaje en ella.</span><span class="sxs-lookup"><span data-stu-id="4d694-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="4d694-109">El objeto de formulario y su interfaz persisten hasta que el usuario lo cierra.</span><span class="sxs-lookup"><span data-stu-id="4d694-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="4d694-110">El objeto form controla los cambios realizados en los valores de las propiedades del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4d694-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="4d694-111">Además, las interfaces de formulario MAPI definen un mecanismo mediante el cual un objeto de formulario puede cargar y mostrar una serie de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4d694-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="4d694-112">Se trata de un mecanismo de eficiencia, ya que evita la destrucción y la creación de objetos de mensaje y sus interfaces.</span><span class="sxs-lookup"><span data-stu-id="4d694-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="4d694-113">Cuando el cliente de mensajería lo solicite para cargar un mensaje diferente, el objeto de formulario debe guardar cualquier cambio en las propiedades del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="4d694-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="4d694-114">Para obtener información sobre la perspectiva de objetos de formulario de una aplicación cliente, vea [Objetos de formulario personalizados MAPI](mapi-custom-form-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4d694-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4d694-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d694-115">See also</span></span>



[<span data-ttu-id="4d694-116">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="4d694-116">MAPI Forms</span></span>](mapi-forms.md)

