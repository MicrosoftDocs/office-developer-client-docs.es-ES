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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327492"
---
# <a name="form-verbs"></a><span data-ttu-id="29a08-103">Verbos de formulario</span><span class="sxs-lookup"><span data-stu-id="29a08-103">Form verbs</span></span>

<span data-ttu-id="29a08-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29a08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29a08-105">La interfaz de usuario de un formulario suele ofrecer elementos de menú o controles que permiten a los usuarios realizar algún tipo de acción con el formulario.</span><span class="sxs-lookup"><span data-stu-id="29a08-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="29a08-106">El trabajo del servidor de formularios controla estas acciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="29a08-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="29a08-107">Esta interfaz se implementa mediante las API de Win32 estándar; escribir una es igual que escribir otras interfaces para los programas Win32 normales.</span><span class="sxs-lookup"><span data-stu-id="29a08-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="29a08-108">Con frecuencia, las acciones del usuario están asociadas con verbos.</span><span class="sxs-lookup"><span data-stu-id="29a08-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="29a08-109">Un verbo es el nombre de una acción específica de una clase de mensaje determinada.</span><span class="sxs-lookup"><span data-stu-id="29a08-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="29a08-110">Por ejemplo, **reply** es un verbo que implementan varios servidores de formularios, cada uno de los cuales puede tener una interpretación diferente de ese verbo.</span><span class="sxs-lookup"><span data-stu-id="29a08-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="29a08-111">A veces, los verbos se denominan comandos.</span><span class="sxs-lookup"><span data-stu-id="29a08-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="29a08-112">No todos los elementos de menú y los controles de un formulario corresponden a un verbo.</span><span class="sxs-lookup"><span data-stu-id="29a08-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="29a08-113">Por ejemplo, un botón **Cancelar** no se corresponde con un verbo de cancelación dentro del servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="29a08-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="29a08-114">Normalmente, los verbos están asociados a acciones específicas de una clase de mensaje determinada o un conjunto de clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="29a08-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="29a08-115">Aunque diferentes clases de mensaje pueden admitir distintos conjuntos de verbos, todos admiten al menos el verbo abrir, que muestra la interfaz de usuario del formulario y lo carga con los valores de propiedad del mensaje.</span><span class="sxs-lookup"><span data-stu-id="29a08-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="29a08-116">Los verbos pueden no tener ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="29a08-116">Verbs may take no parameters.</span></span> <span data-ttu-id="29a08-117">Los formularios que exportan comandos con parámetros de variable deben usar los mecanismos de automatización.</span><span class="sxs-lookup"><span data-stu-id="29a08-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="29a08-118">Los clientes pueden determinar qué verbos admite una clase de mensaje determinada a través del método [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) , implementado por el administrador de formularios MAPI.</span><span class="sxs-lookup"><span data-stu-id="29a08-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="29a08-119">El administrador de formularios obtiene esta información del archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="29a08-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="29a08-120">El cliente usa el conjunto de verbos devuelto por este método para mostrar al usuario qué comandos se pueden ejecutar en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="29a08-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="29a08-121">Por ejemplo, es posible que un cliente permita a los usuarios hacer clic con el botón secundario del mouse en un mensaje para mostrar verbos aplicables a ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="29a08-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="29a08-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="29a08-122">See also</span></span>

- [<span data-ttu-id="29a08-123">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="29a08-123">MAPI Forms</span></span>](mapi-forms.md)

