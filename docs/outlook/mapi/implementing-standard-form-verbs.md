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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426124"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="191e4-103">Implementación de verbos de formulario estándar</span><span class="sxs-lookup"><span data-stu-id="191e4-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="191e4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="191e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="191e4-105">MAPI define un conjunto de verbos estándar, o acciones realizadas cuando un usuario hace una selección de menú o hace clic en un botón, que todos los visores de formularios deben admitir.</span><span class="sxs-lookup"><span data-stu-id="191e4-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="191e4-106">Cada verbo tiene una constante asociada para su identificación, definida en el EXCHFORM. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="191e4-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="191e4-107">En la tabla siguiente se enumeran los verbos de formulario estándar y sus constantes asociadas:</span><span class="sxs-lookup"><span data-stu-id="191e4-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="191e4-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="191e4-108">**Verb**</span></span>|<span data-ttu-id="191e4-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="191e4-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="191e4-110">Abrir</span><span class="sxs-lookup"><span data-stu-id="191e4-110">Open</span></span>  <br/> |<span data-ttu-id="191e4-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="191e4-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="191e4-112">Responder</span><span class="sxs-lookup"><span data-stu-id="191e4-112">Reply</span></span>  <br/> |<span data-ttu-id="191e4-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="191e4-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="191e4-114">Responder a todos</span><span class="sxs-lookup"><span data-stu-id="191e4-114">Reply to All</span></span>  <br/> |<span data-ttu-id="191e4-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="191e4-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="191e4-116">Reenviar</span><span class="sxs-lookup"><span data-stu-id="191e4-116">Forward</span></span>  <br/> |<span data-ttu-id="191e4-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="191e4-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="191e4-118">Imprimir</span><span class="sxs-lookup"><span data-stu-id="191e4-118">Print</span></span>  <br/> |<span data-ttu-id="191e4-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="191e4-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="191e4-120">Guardar como</span><span class="sxs-lookup"><span data-stu-id="191e4-120">Save As</span></span>  <br/> |<span data-ttu-id="191e4-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="191e4-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="191e4-122">Responder en carpeta</span><span class="sxs-lookup"><span data-stu-id="191e4-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="191e4-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="191e4-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="191e4-124">Cuando un usuario elige un verbo, pasa su constante en una llamada al método [IMAPIForm::D oVerb](imapiform-doverb.md) del formulario para realizar la acción correspondiente.</span><span class="sxs-lookup"><span data-stu-id="191e4-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="191e4-125">Además de tener acceso a verbos a través del visor de formularios, los usuarios a veces pueden tener acceso a verbos directamente desde el formulario.</span><span class="sxs-lookup"><span data-stu-id="191e4-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="191e4-126">Por ejemplo, algunos objetos de formulario permiten al usuario invocar el verbo  **Imprimir** haciendo clic con el botón secundario en el formulario y eligiendo Imprimir en un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="191e4-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

