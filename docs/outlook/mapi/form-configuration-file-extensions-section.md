---
title: Sección Archivo de configuración de formulario [Extensiones]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423758"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="79e12-103">Sección Archivo de configuración de formulario [Extensiones]</span><span class="sxs-lookup"><span data-stu-id="79e12-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="79e12-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79e12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79e12-105">La **sección [Extensiones]** enumera los atributos extendidos del formulario, normalmente un conjunto de propiedades con nombre, que son atributos que van más allá de los básicos enumerados en la sección **[Descripción]** del archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="79e12-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="79e12-106">Los atributos extendidos son propiedades devueltas de llamadas al **método GetProps** del objeto **IMAPIFormInfo** con el conjunto de bits alto en la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="79e12-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="79e12-107">Las aplicaciones cliente pueden determinar los atributos extendidos de un formulario, si los hay, recuperando estas etiquetas.</span><span class="sxs-lookup"><span data-stu-id="79e12-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="79e12-108">Para ello, los clientes llaman al método [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) pasando los nombres de las propiedades del formulario y llaman al método [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="79e12-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="79e12-109">**[Extensiones]**</span><span class="sxs-lookup"><span data-stu-id="79e12-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="79e12-110">**Extensión.**</span><span class="sxs-lookup"><span data-stu-id="79e12-110">**Extension.**</span></span> <span data-ttu-id="79e12-111">_string1_  =   _string2_</span><span class="sxs-lookup"><span data-stu-id="79e12-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="79e12-112">Cada sección de propiedad de extensión define un atributo de extensión mediante la sintaxis de propiedad con nombre MAPI.</span><span class="sxs-lookup"><span data-stu-id="79e12-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="79e12-113">El tipo de propiedad debe ser PT_LONG o PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="79e12-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="79e12-114">No se admiten los conjuntos de propiedades que contienen cadenas con nombre.</span><span class="sxs-lookup"><span data-stu-id="79e12-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="79e12-115">El formato de la **sección [Extensión]** es:</span><span class="sxs-lookup"><span data-stu-id="79e12-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="79e12-116">**[Extensión.**</span><span class="sxs-lookup"><span data-stu-id="79e12-116">**[Extension.**</span></span> <span data-ttu-id="79e12-117">_string2_ **]**</span><span class="sxs-lookup"><span data-stu-id="79e12-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="79e12-118">**Tipo**  =   _entero_</span><span class="sxs-lookup"><span data-stu-id="79e12-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="79e12-119">**NmidPropset**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="79e12-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="79e12-120">**NmidInteger**  =   _entero_</span><span class="sxs-lookup"><span data-stu-id="79e12-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="79e12-121">**Valor**  =   _string_  |   _entero_</span><span class="sxs-lookup"><span data-stu-id="79e12-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="79e12-122">A continuación se muestra un ejemplo de una **sección [Extensiones]** y una sección relacionada posterior.</span><span class="sxs-lookup"><span data-stu-id="79e12-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


