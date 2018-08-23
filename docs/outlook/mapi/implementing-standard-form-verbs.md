---
title: Implementar verbos estándar del formulario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 46585859e1dde4ecf38262f99cac5e3a9d29e5db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568752"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="5e68f-103">Implementar verbos estándar del formulario</span><span class="sxs-lookup"><span data-stu-id="5e68f-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="5e68f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e68f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e68f-105">MAPI define un conjunto de verbos estándar o acciones llevadas a cabo cuando un usuario realiza una selección de menú o hace clic en un botón, que deben admitir todos los visores de formulario.</span><span class="sxs-lookup"><span data-stu-id="5e68f-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="5e68f-106">Cada verbo tiene una constante asociada para la identificación, definido en el EXCHFORM. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="5e68f-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="5e68f-107">En la siguiente tabla se enumera los verbos de formulario estándar y sus constantes asociadas:</span><span class="sxs-lookup"><span data-stu-id="5e68f-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="5e68f-108">**Verbo**</span><span class="sxs-lookup"><span data-stu-id="5e68f-108">**Verb**</span></span>|<span data-ttu-id="5e68f-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5e68f-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e68f-110">Abrir</span><span class="sxs-lookup"><span data-stu-id="5e68f-110">Open</span></span>  <br/> |<span data-ttu-id="5e68f-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="5e68f-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="5e68f-112">Responder</span><span class="sxs-lookup"><span data-stu-id="5e68f-112">Reply</span></span>  <br/> |<span data-ttu-id="5e68f-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="5e68f-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="5e68f-114">Responder a todos</span><span class="sxs-lookup"><span data-stu-id="5e68f-114">Reply to All</span></span>  <br/> |<span data-ttu-id="5e68f-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="5e68f-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="5e68f-116">Forward</span><span class="sxs-lookup"><span data-stu-id="5e68f-116">Forward</span></span>  <br/> |<span data-ttu-id="5e68f-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="5e68f-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="5e68f-118">Imprimir</span><span class="sxs-lookup"><span data-stu-id="5e68f-118">Print</span></span>  <br/> |<span data-ttu-id="5e68f-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="5e68f-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="5e68f-120">Guardar como</span><span class="sxs-lookup"><span data-stu-id="5e68f-120">Save As</span></span>  <br/> |<span data-ttu-id="5e68f-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="5e68f-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="5e68f-122">Responder en carpeta</span><span class="sxs-lookup"><span data-stu-id="5e68f-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="5e68f-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="5e68f-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="5e68f-124">Cuando un usuario elige un verbo, pase la constante en la llamada al método de [IMAPIForm::DoVerb](imapiform-doverb.md) del formulario que realice su acción correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5e68f-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="5e68f-125">Además de obtener acceso a los verbos de a través de su Visor de formulario, los usuarios pueden acceder a veces verbos directamente desde el formulario.</span><span class="sxs-lookup"><span data-stu-id="5e68f-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="5e68f-126">Por ejemplo, algunos objetos de formulario permiten al usuario invocar el verbo **Imprimir** haciendo doble clic en el formulario y eligiendo **Print** en un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="5e68f-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

