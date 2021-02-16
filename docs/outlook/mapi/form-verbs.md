---
title: Verbos de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: dbd08437dfdd38c3a43cbf12eae8710cc8e3661e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424031"
---
# <a name="form-verbs"></a><span data-ttu-id="afd6c-103">Verbos de formulario</span><span class="sxs-lookup"><span data-stu-id="afd6c-103">Form verbs</span></span>

<span data-ttu-id="afd6c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="afd6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="afd6c-105">La interfaz de usuario de un formulario normalmente ofrece elementos de menú o controles que permiten a los usuarios realizar algún tipo de acción con el formulario.</span><span class="sxs-lookup"><span data-stu-id="afd6c-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="afd6c-106">El trabajo del servidor de formularios es controlar estas acciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="afd6c-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="afd6c-107">Esta interfaz se implementa mediante las API estándar de Win32; escribir una es igual que escribir otras interfaces para programas normales de Win32.</span><span class="sxs-lookup"><span data-stu-id="afd6c-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="afd6c-108">A menudo, las acciones del usuario se asocian con verbos.</span><span class="sxs-lookup"><span data-stu-id="afd6c-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="afd6c-109">Un verbo es el nombre de una acción específica de una clase de mensaje determinada.</span><span class="sxs-lookup"><span data-stu-id="afd6c-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="afd6c-110">Por ejemplo, **Responder** es un verbo que implementan muchos servidores de formulario, cada uno de los cuales puede tener una interpretación diferente de ese verbo.</span><span class="sxs-lookup"><span data-stu-id="afd6c-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="afd6c-111">A veces, los verbos se denominan comandos.</span><span class="sxs-lookup"><span data-stu-id="afd6c-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="afd6c-112">No todos los elementos de menú y controles de un formulario corresponden a un verbo.</span><span class="sxs-lookup"><span data-stu-id="afd6c-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="afd6c-113">Por ejemplo, un **botón Cancelar** no corresponde a un verbo Cancel dentro del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="afd6c-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="afd6c-114">Normalmente, los verbos se asocian con acciones específicas de una clase de mensaje determinada o un conjunto de clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="afd6c-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="afd6c-115">Aunque diferentes clases de mensajes pueden admitir distintos conjuntos de verbos, todos admiten al menos el verbo Open, que muestra la interfaz de usuario del formulario y la carga con los valores de propiedad del mensaje.</span><span class="sxs-lookup"><span data-stu-id="afd6c-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="afd6c-116">Es posible que los verbos no tomen ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="afd6c-116">Verbs may take no parameters.</span></span> <span data-ttu-id="afd6c-117">Los formularios que exportan comandos con parámetros variables deben usar los mecanismos de automatización.</span><span class="sxs-lookup"><span data-stu-id="afd6c-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="afd6c-118">Los clientes pueden determinar qué verbos son compatibles con una clase de mensaje determinada mediante el método [IMAPIFormInfo::CalcVerbSet,](imapiforminfo-calcverbset.md) que implementa el administrador de formularios MAPI.</span><span class="sxs-lookup"><span data-stu-id="afd6c-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="afd6c-119">El administrador del formulario obtiene esta información del archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="afd6c-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="afd6c-120">El cliente usa el conjunto de verbos devuelto por este método para mostrar al usuario qué comandos se pueden ejecutar en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="afd6c-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="afd6c-121">Por ejemplo, un cliente puede permitir a los usuarios hacer clic con el botón secundario del mouse sobre un mensaje para mostrar verbos aplicables a ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="afd6c-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="afd6c-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="afd6c-122">See also</span></span>

- [<span data-ttu-id="afd6c-123">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="afd6c-123">MAPI Forms</span></span>](mapi-forms.md)

