---
title: Verbos de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 1ecc80feec2b0a86f35d03f1ca4f75ea9ff094e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816854"
---
# <a name="form-verbs"></a><span data-ttu-id="88e44-103">Verbos de formulario</span><span class="sxs-lookup"><span data-stu-id="88e44-103">Form verbs</span></span>

<span data-ttu-id="88e44-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88e44-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88e44-105">Normalmente, la interfaz de usuario de un formulario ofrece los elementos de menú o los controles que permiten a los usuarios realizar algún tipo de acción con el formulario.</span><span class="sxs-lookup"><span data-stu-id="88e44-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="88e44-106">Es del servidor formulario para controlar las acciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="88e44-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="88e44-107">Esta interfaz se implementa mediante las API de Win32 estándar; escribir uno es igual que escribir otras interfaces de programas de Win32 normales.</span><span class="sxs-lookup"><span data-stu-id="88e44-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="88e44-108">A menudo, las acciones del usuario se asocian con los verbos.</span><span class="sxs-lookup"><span data-stu-id="88e44-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="88e44-109">Un verbo es el nombre de una acción que es específico de una determinada clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="88e44-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="88e44-110">Por ejemplo, la **respuesta** es un verbo que se implementa mediante muchos servidores de formulario, cada uno de los cuales puede tener una interpretación diferente de ese verbo.</span><span class="sxs-lookup"><span data-stu-id="88e44-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="88e44-111">A veces se hace referencia a verbos como comandos.</span><span class="sxs-lookup"><span data-stu-id="88e44-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="88e44-112">No todos los elementos de menú y controles de un formulario se corresponden con un verbo.</span><span class="sxs-lookup"><span data-stu-id="88e44-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="88e44-113">Por ejemplo, un botón **Cancelar** no corresponde a un verbo Cancelar dentro del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="88e44-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="88e44-114">Normalmente, los verbos están asociados con las acciones que son específicas de una clase de mensaje concreto o un conjunto de clases de mensajes.</span><span class="sxs-lookup"><span data-stu-id="88e44-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="88e44-115">Aunque las clases de mensajes diferentes pueden admitir distintos conjuntos de verbos, todos admiten al menos el verbo Open, que muestra la interfaz de usuario del formulario y carga con valores de propiedad del mensaje.</span><span class="sxs-lookup"><span data-stu-id="88e44-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="88e44-116">Los verbos no pueden tardar parámetros.</span><span class="sxs-lookup"><span data-stu-id="88e44-116">Verbs may take no parameters.</span></span> <span data-ttu-id="88e44-117">Los formularios que exportación comandos con parámetros variables deben utilizar los mecanismos de automatización.</span><span class="sxs-lookup"><span data-stu-id="88e44-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="88e44-118">Los clientes pueden determinar qué verbos son compatibles con una clase de mensaje en particular a través del método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) , que se implementa mediante el Administrador de formularios de MAPI.</span><span class="sxs-lookup"><span data-stu-id="88e44-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="88e44-119">El Administrador de formulario obtiene esta información desde el archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="88e44-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="88e44-120">El conjunto de verbos devueltos por este método se usa en el cliente para mostrar al usuario los comandos que se pueden ejecutar en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="88e44-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="88e44-121">Por ejemplo, un cliente es posible que permiten a los usuarios haga clic en el botón secundario del mouse a través de un mensaje para mostrar los verbos aplicables a ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="88e44-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="88e44-122">Ver también</span><span class="sxs-lookup"><span data-stu-id="88e44-122">See also</span></span>

- [<span data-ttu-id="88e44-123">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="88e44-123">MAPI Forms</span></span>](mapi-forms.md)

