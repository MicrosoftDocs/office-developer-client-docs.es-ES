---
title: Sección Archivo de configuración de formulario [Verbos]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417787"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="bcacd-103">Sección Archivo de configuración de formulario [Verbos]</span><span class="sxs-lookup"><span data-stu-id="bcacd-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="bcacd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcacd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcacd-105">La **sección [Verbos]** enumera el conjunto completo de verbos admitidos por el formulario.</span><span class="sxs-lookup"><span data-stu-id="bcacd-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="bcacd-106">El formato de la **sección [Verbos]** es:</span><span class="sxs-lookup"><span data-stu-id="bcacd-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="bcacd-107">**[Verbos]**</span><span class="sxs-lookup"><span data-stu-id="bcacd-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="bcacd-108">**Verb1**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="bcacd-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="bcacd-109">A continuación se muestra un ejemplo de **una sección [Verbos].**</span><span class="sxs-lookup"><span data-stu-id="bcacd-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="bcacd-110">Cada verbo se define en un **[Verbo] independiente.**</span><span class="sxs-lookup"><span data-stu-id="bcacd-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="bcacd-111">_string_ **]** section.</span><span class="sxs-lookup"><span data-stu-id="bcacd-111">_string_ **]** section.</span></span> <span data-ttu-id="bcacd-112">A **[Verbo.**</span><span class="sxs-lookup"><span data-stu-id="bcacd-112">A **[Verb.**</span></span> <span data-ttu-id="bcacd-113">_la_ **sección string ]** describe un solo verbo ofrecido por el formulario.</span><span class="sxs-lookup"><span data-stu-id="bcacd-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="bcacd-114">La **entrada DisplayName** en **un [Verbo.**</span><span class="sxs-lookup"><span data-stu-id="bcacd-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="bcacd-115">_la_ **sección string ]** especifica el nombre del comando que se muestra en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="bcacd-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="bcacd-116">La **entrada** Code corresponde al número de verbo pasado en el [método IMAPIForm::D oVerb.](imapiform-doverb.md)</span><span class="sxs-lookup"><span data-stu-id="bcacd-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="bcacd-117">Sintaxis de **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="bcacd-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="bcacd-118">_la_ **sección de cadena ]** es:</span><span class="sxs-lookup"><span data-stu-id="bcacd-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="bcacd-119">**[Verbo.**</span><span class="sxs-lookup"><span data-stu-id="bcacd-119">**[Verb.**</span></span> <span data-ttu-id="bcacd-120">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="bcacd-120">_string_ **]**</span></span>
  
 <span data-ttu-id="bcacd-121">**DisplayName**  =   _cadena mostrada_</span><span class="sxs-lookup"><span data-stu-id="bcacd-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="bcacd-122">**Código**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="bcacd-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="bcacd-123">**Flags**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="bcacd-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="bcacd-124">**Attribs**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="bcacd-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="bcacd-125">A continuación se muestra un ejemplo **de un [Verbo.**</span><span class="sxs-lookup"><span data-stu-id="bcacd-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="bcacd-126">_string_ **]** section.</span><span class="sxs-lookup"><span data-stu-id="bcacd-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="bcacd-127">Los verbos enumerados en esta sección los recupera un cliente mediante el método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="bcacd-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="bcacd-128">Los verbos se activan llamando al método [IMAPIForm::D oVerb](imapiform-doverb.md) del formulario y pasando el número de código del verbo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="bcacd-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

