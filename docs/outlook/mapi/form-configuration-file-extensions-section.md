---
title: Sección del archivo de configuración de formulario [extensiones]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327303"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="08b47-103">Sección del archivo de configuración de formulario [extensiones]</span><span class="sxs-lookup"><span data-stu-id="08b47-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="08b47-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08b47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08b47-105">La sección **[extensions]** enumera los atributos extendidos del formulario, normalmente un conjunto de propiedades con nombre, que son todos los atributos que se encuentran fuera de los elementos básicos que aparecen en la sección **[Description]** del archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="08b47-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="08b47-106">Los atributos extendidos son propiedades que devuelven las llamadas al método **GetProps** del objeto **IMAPIFormInfo** con el bit alto establecido en la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="08b47-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="08b47-107">Las aplicaciones cliente pueden determinar los atributos extendidos de un formulario, si los hay, mediante la recuperación de estas etiquetas.</span><span class="sxs-lookup"><span data-stu-id="08b47-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="08b47-108">Para ello, los clientes llaman al método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) , pasando los nombres de las propiedades del formulario y llaman al método [IMAPIProp:: GetProps](imapiprop-getprops.md) para obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="08b47-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="08b47-109">**Prórroga**</span><span class="sxs-lookup"><span data-stu-id="08b47-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="08b47-110">**Extensión.**</span><span class="sxs-lookup"><span data-stu-id="08b47-110">**Extension.**</span></span> <span data-ttu-id="08b47-111">_cadena1_ =  _cadena2_</span><span class="sxs-lookup"><span data-stu-id="08b47-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="08b47-112">Cada sección de propiedad de extensión define un atributo de extensión mediante la sintaxis de propiedad denominada MAPI.</span><span class="sxs-lookup"><span data-stu-id="08b47-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="08b47-113">El tipo de propiedad debe ser PT_LONG o PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="08b47-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="08b47-114">Los conjuntos de propiedades que contienen cadenas con nombre no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="08b47-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="08b47-115">El formato de la sección **[Extension]** es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="08b47-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="08b47-116">**Extensión.**</span><span class="sxs-lookup"><span data-stu-id="08b47-116">**[Extension.**</span></span> <span data-ttu-id="08b47-117">_cadena2_ **]**</span><span class="sxs-lookup"><span data-stu-id="08b47-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="08b47-118">**Tipo** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="08b47-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="08b47-119">\*\*\*\* =  _GUID_ de NmidPropset</span><span class="sxs-lookup"><span data-stu-id="08b47-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="08b47-120">\*\*\*\* =  _Entero_ NmidInteger</span><span class="sxs-lookup"><span data-stu-id="08b47-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="08b47-121">\*\*\*\* =  __ |  _Entero_ de cadena de valor</span><span class="sxs-lookup"><span data-stu-id="08b47-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="08b47-122">A continuación se muestra un ejemplo de una sección **[extensions]** y una sección relacionada subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="08b47-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


