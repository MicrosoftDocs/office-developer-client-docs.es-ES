---
title: Sección del archivo de configuración de formulario [Extensiones]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7c26b86ad4d6c7fd565abddbfc76f50ac3dccaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816834"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="d3af6-103">Sección del archivo de configuración de formulario [Extensiones]</span><span class="sxs-lookup"><span data-stu-id="d3af6-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="d3af6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3af6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3af6-105">La sección **[Extensions]** enumera los atributos extendidos del formulario, normalmente un conjunto de propiedades con nombre, que son los atributos más allá de los básicos que aparecen en la sección **[descripción]** del archivo de configuración de formulario.</span><span class="sxs-lookup"><span data-stu-id="d3af6-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="d3af6-106">Atributos extendidos no son propiedades devueltas de las llamadas al método **GetProps** del objeto **IMAPIFormInfo** con el bit alto establecido en la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d3af6-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="d3af6-107">Las aplicaciones cliente pueden determinar los atributos extendidos de un formulario, si hay alguno, mediante la recuperación de estas etiquetas.</span><span class="sxs-lookup"><span data-stu-id="d3af6-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="d3af6-108">Para ello, los clientes de llamar al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , pasando en los nombres de las propiedades del formulario y llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="d3af6-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="d3af6-109">**[Extensions]**</span><span class="sxs-lookup"><span data-stu-id="d3af6-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="d3af6-110">**Extensión.**</span><span class="sxs-lookup"><span data-stu-id="d3af6-110">**Extension.**</span></span> <span data-ttu-id="d3af6-111">_cadena1_ =  _cadena2_</span><span class="sxs-lookup"><span data-stu-id="d3af6-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="d3af6-112">Cada sección de la propiedad de extensión define un atributo de extensión mediante la con el nombre de sintaxis de la propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="d3af6-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="d3af6-113">El tipo de propiedad debe ser PT_LONG o PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="d3af6-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="d3af6-114">No se admiten los conjuntos de propiedades que contiene las cadenas con nombre.</span><span class="sxs-lookup"><span data-stu-id="d3af6-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="d3af6-115">El formato de la sección **[extensión]** es:</span><span class="sxs-lookup"><span data-stu-id="d3af6-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="d3af6-116">**[Extensión.**</span><span class="sxs-lookup"><span data-stu-id="d3af6-116">**[Extension.**</span></span> <span data-ttu-id="d3af6-117">_cadena2_ **]**</span><span class="sxs-lookup"><span data-stu-id="d3af6-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="d3af6-118">**Tipo de** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="d3af6-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="d3af6-119">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="d3af6-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="d3af6-120">**NmidInteger** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="d3af6-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="d3af6-121">**Valor** =  _cadena_ |  _entero_</span><span class="sxs-lookup"><span data-stu-id="d3af6-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="d3af6-122">Se muestra un ejemplo de una sección **[Extensions]** y una sección posterior relacionada siguientes.</span><span class="sxs-lookup"><span data-stu-id="d3af6-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


