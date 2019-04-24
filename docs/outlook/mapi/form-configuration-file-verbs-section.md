---
title: Sección del archivo de configuración de formulario [verbos]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327499"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="6794e-103">Sección del archivo de configuración de formulario [verbos]</span><span class="sxs-lookup"><span data-stu-id="6794e-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="6794e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6794e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6794e-105">La sección **[verbs]** muestra el conjunto completo de verbos admitidos por el formulario.</span><span class="sxs-lookup"><span data-stu-id="6794e-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="6794e-106">El formato de la sección **[verbs]** es:</span><span class="sxs-lookup"><span data-stu-id="6794e-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="6794e-107">**Verbos**</span><span class="sxs-lookup"><span data-stu-id="6794e-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="6794e-108">\*\*\*\* =  _Cadena_ Verb1</span><span class="sxs-lookup"><span data-stu-id="6794e-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="6794e-109">A continuación se encuentra un ejemplo de una sección **[verbs]** .</span><span class="sxs-lookup"><span data-stu-id="6794e-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="6794e-110">Cada verbo se define en un **[verbo.**</span><span class="sxs-lookup"><span data-stu-id="6794e-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="6794e-111">_cadena_ de **]** sección.</span><span class="sxs-lookup"><span data-stu-id="6794e-111">_string_ **]** section.</span></span> <span data-ttu-id="6794e-112">**[Verbo.**</span><span class="sxs-lookup"><span data-stu-id="6794e-112">A **[Verb.**</span></span> <span data-ttu-id="6794e-113">_cadena_ de **]** describe un único Verbo ofrecido por el formulario.</span><span class="sxs-lookup"><span data-stu-id="6794e-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="6794e-114">La entrada **displayName** en **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="6794e-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="6794e-115">_cadena_ de **]** especifica el nombre de comando que se muestra en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6794e-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="6794e-116">La entrada de **código** corresponde al número de verbo pasado en el método [IMAPIForm::D overb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="6794e-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="6794e-117">La sintaxis del **verbo.**</span><span class="sxs-lookup"><span data-stu-id="6794e-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="6794e-118">_cadena_ de **]** es:</span><span class="sxs-lookup"><span data-stu-id="6794e-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="6794e-119">**Verbo.**</span><span class="sxs-lookup"><span data-stu-id="6794e-119">**[Verb.**</span></span> <span data-ttu-id="6794e-120">_cadena_ de **]**</span><span class="sxs-lookup"><span data-stu-id="6794e-120">_string_ **]**</span></span>
  
 <span data-ttu-id="6794e-121">\*\*\*\* =  _Cadena mostrada_ como DisplayName</span><span class="sxs-lookup"><span data-stu-id="6794e-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="6794e-122">\*\*\*\* =  _Número entero_ del código</span><span class="sxs-lookup"><span data-stu-id="6794e-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="6794e-123">**Indicadores** =  _enteros_</span><span class="sxs-lookup"><span data-stu-id="6794e-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="6794e-124">\*\*\*\* =  _Entero_ attribs</span><span class="sxs-lookup"><span data-stu-id="6794e-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="6794e-125">A continuación se encuentra un ejemplo de **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="6794e-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="6794e-126">_cadena_ de **]** sección.</span><span class="sxs-lookup"><span data-stu-id="6794e-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="6794e-127">Los verbos que se enumeran en esta sección los recupera un cliente mediante el [método IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="6794e-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="6794e-128">Los verbos se activan llamando al método [IMAPIForm::D overb](imapiform-doverb.md) del formulario y pasándole el número de código del verbo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="6794e-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

