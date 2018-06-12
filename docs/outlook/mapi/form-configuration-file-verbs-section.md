---
title: Sección de [verbos] del archivo de configuración de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 5fe1b064b48bc9112a872677fbf5042b7dfe5449
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816851"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="7580d-103">Sección de [verbos] del archivo de configuración de formulario</span><span class="sxs-lookup"><span data-stu-id="7580d-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="7580d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7580d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7580d-105">La sección **[verbos]** enumera todo el conjunto de verbos admitidos por el formulario.</span><span class="sxs-lookup"><span data-stu-id="7580d-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="7580d-106">El formato de la sección **[verbos]** es:</span><span class="sxs-lookup"><span data-stu-id="7580d-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="7580d-107">**[Verbos]**</span><span class="sxs-lookup"><span data-stu-id="7580d-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="7580d-108">**Verb1** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="7580d-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="7580d-109">Siguiente es un ejemplo de una sección **[verbos]** .</span><span class="sxs-lookup"><span data-stu-id="7580d-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="7580d-110">Se define cada verbo en un independiente **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="7580d-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="7580d-111">_cadena_ sección **]** .</span><span class="sxs-lookup"><span data-stu-id="7580d-111">_string_ **]** section.</span></span> <span data-ttu-id="7580d-112">A **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="7580d-112">A **[Verb.**</span></span> <span data-ttu-id="7580d-113">_cadena_ **]** sección describe un solo verbo ofrecido por el formulario.</span><span class="sxs-lookup"><span data-stu-id="7580d-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="7580d-114">La entrada **DisplayName** en un **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="7580d-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="7580d-115">_cadena_ sección **]** especifica el nombre del comando que se muestra en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7580d-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="7580d-116">La entrada de **código** se corresponde con el número de verbo que se pasa en el método [IMAPIForm::DoVerb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="7580d-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="7580d-117">La sintaxis de la **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="7580d-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="7580d-118">_cadena_ sección **]** es:</span><span class="sxs-lookup"><span data-stu-id="7580d-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="7580d-119">**[Verbo.**</span><span class="sxs-lookup"><span data-stu-id="7580d-119">**[Verb.**</span></span> <span data-ttu-id="7580d-120">_cadena_ **]**</span><span class="sxs-lookup"><span data-stu-id="7580d-120">_string_ **]**</span></span>
  
 <span data-ttu-id="7580d-121">**DisplayName** =  _muestra la cadena_</span><span class="sxs-lookup"><span data-stu-id="7580d-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="7580d-122">**Código** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="7580d-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="7580d-123">**Marcas de** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="7580d-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="7580d-124">**Se utilizaron atributos** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="7580d-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="7580d-125">A continuación se incluye un ejemplo de un **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="7580d-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="7580d-126">_cadena_ sección **]** .</span><span class="sxs-lookup"><span data-stu-id="7580d-126">_string_ **]** section.</span></span> 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

<span data-ttu-id="7580d-127">Verbos enumerados en esta sección se recuperan mediante un cliente mediante el [método IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="7580d-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="7580d-128">Verbos se activan al llamar al método [IMAPIForm::DoVerb](imapiform-doverb.md) del formulario y pasar el número de código del verbo que se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="7580d-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

