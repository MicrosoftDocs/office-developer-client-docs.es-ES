---
title: Implementación de verbos de formulario estándar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317447"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="4fc59-103">Implementación de verbos de formulario estándar</span><span class="sxs-lookup"><span data-stu-id="4fc59-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="4fc59-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fc59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fc59-105">MAPI define un conjunto de verbos estándar o acciones realizadas cuando un usuario hace una selección de menú o hace clic en un botón, que deben admitir todas las vistas de formulario.</span><span class="sxs-lookup"><span data-stu-id="4fc59-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="4fc59-106">Cada verbo tiene una constante asociada para la identificación, definida en el EXCHFORM. H archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="4fc59-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="4fc59-107">En la siguiente tabla se enumeran los verbos de formulario estándar y sus constantes asociadas:</span><span class="sxs-lookup"><span data-stu-id="4fc59-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="4fc59-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="4fc59-108">**Verb**</span></span>|<span data-ttu-id="4fc59-109">**Value**</span><span class="sxs-lookup"><span data-stu-id="4fc59-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4fc59-110">Abrir</span><span class="sxs-lookup"><span data-stu-id="4fc59-110">Open</span></span>  <br/> |<span data-ttu-id="4fc59-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="4fc59-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="4fc59-112">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4fc59-112">Reply</span></span>  <br/> |<span data-ttu-id="4fc59-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="4fc59-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="4fc59-114">Responder a todos</span><span class="sxs-lookup"><span data-stu-id="4fc59-114">Reply to All</span></span>  <br/> |<span data-ttu-id="4fc59-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="4fc59-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="4fc59-116">Forward</span><span class="sxs-lookup"><span data-stu-id="4fc59-116">Forward</span></span>  <br/> |<span data-ttu-id="4fc59-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="4fc59-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="4fc59-118">Print</span><span class="sxs-lookup"><span data-stu-id="4fc59-118">Print</span></span>  <br/> |<span data-ttu-id="4fc59-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="4fc59-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="4fc59-120">Guardar como</span><span class="sxs-lookup"><span data-stu-id="4fc59-120">Save As</span></span>  <br/> |<span data-ttu-id="4fc59-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="4fc59-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="4fc59-122">Responder en carpeta</span><span class="sxs-lookup"><span data-stu-id="4fc59-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="4fc59-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="4fc59-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="4fc59-124">Cuando un usuario elige un verbo, pasa su constante en una llamada al método [IMAPIForm::D overb](imapiform-doverb.md) del formulario para realizar su acción correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4fc59-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="4fc59-125">Además de tener acceso a los verbos a través del visor de formularios, los usuarios pueden tener acceso a verbos directamente desde el formulario.</span><span class="sxs-lookup"><span data-stu-id="4fc59-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="4fc59-126">Por ejemplo, algunos objetos Form permiten al usuario invocar el verbo **Imprimir** haciendo clic con el botón secundario en el formulario y eligiendo **Imprimir** desde un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="4fc59-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

