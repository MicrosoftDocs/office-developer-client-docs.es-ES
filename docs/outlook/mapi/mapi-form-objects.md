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
ms.openlocfilehash: 0cece598d4ad337e29edb3bb98b302de900e056d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593469"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="6df65-103">Objetos de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="6df65-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="6df65-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6df65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6df65-105">Objetos de formulario se crean dinámicamente por los servidores de formulario a fin de mostrar mensajes específicos y permitir a los usuarios interactuar con ellos.</span><span class="sxs-lookup"><span data-stu-id="6df65-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="6df65-106">Un objeto de formulario es, por lo tanto, una creación de instancias de la clase derivada de [IMAPIForm](imapiformiunknown.md) que se implementa mediante el servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="6df65-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="6df65-107">Cuando una aplicación cliente abre un mensaje, el servidor de formulario para esa clase de mensaje crea un objeto de formulario para controlar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6df65-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="6df65-108">A continuación, el objeto de formulario crea su interfaz y muestra las propiedades del mensaje en él.</span><span class="sxs-lookup"><span data-stu-id="6df65-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="6df65-109">El objeto de formulario y su interfaz continúa hasta que el usuario lo cierre.</span><span class="sxs-lookup"><span data-stu-id="6df65-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="6df65-110">El objeto de formulario controla los cambios realizados en los valores de las propiedades del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6df65-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="6df65-111">Además, las interfaces de formulario MAPI definen un mecanismo por el que puede cargar y mostrar una serie de mensajes de un objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="6df65-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="6df65-112">Esto es un mecanismo de eficacia, ya que evita destrucción innecesaria y la creación de objetos de mensaje y sus interfaces.</span><span class="sxs-lookup"><span data-stu-id="6df65-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="6df65-113">Cuando lo solicita el cliente de mensajería para cargar un mensaje distinto, el objeto de formulario debe guardar los cambios a las propiedades del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="6df65-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="6df65-114">Para obtener información sobre la perspectiva de la aplicación cliente de objetos de formulario, vea [Objetos de formulario personalizada de MAPI](mapi-custom-form-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6df65-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6df65-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6df65-115">See also</span></span>



[<span data-ttu-id="6df65-116">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="6df65-116">MAPI Forms</span></span>](mapi-forms.md)

