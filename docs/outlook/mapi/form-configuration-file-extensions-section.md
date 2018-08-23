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
ms.openlocfilehash: 459c5f5a34421583141028cd9accad5e242d31ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573561"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="acf0b-103">Sección del archivo de configuración de formulario [Extensiones]</span><span class="sxs-lookup"><span data-stu-id="acf0b-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="acf0b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acf0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acf0b-105">La sección **[Extensions]** enumera los atributos extendidos del formulario, normalmente un conjunto de propiedades con nombre, que son los atributos más allá de los básicos que aparecen en la sección **[descripción]** del archivo de configuración de formulario.</span><span class="sxs-lookup"><span data-stu-id="acf0b-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="acf0b-106">Atributos extendidos no son propiedades devueltas de las llamadas al método **GetProps** del objeto **IMAPIFormInfo** con el bit alto establecido en la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="acf0b-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="acf0b-107">Las aplicaciones cliente pueden determinar los atributos extendidos de un formulario, si hay alguno, mediante la recuperación de estas etiquetas.</span><span class="sxs-lookup"><span data-stu-id="acf0b-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="acf0b-108">Para ello, los clientes de llamar al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , pasando en los nombres de las propiedades del formulario y llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="acf0b-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="acf0b-109">**[Extensions]**</span><span class="sxs-lookup"><span data-stu-id="acf0b-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="acf0b-110">**Extensión.**</span><span class="sxs-lookup"><span data-stu-id="acf0b-110">**Extension.**</span></span> <span data-ttu-id="acf0b-111">_cadena1_ =  _cadena2_</span><span class="sxs-lookup"><span data-stu-id="acf0b-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="acf0b-112">Cada sección de la propiedad de extensión define un atributo de extensión mediante la con el nombre de sintaxis de la propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="acf0b-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="acf0b-113">El tipo de propiedad debe ser PT_LONG o PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="acf0b-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="acf0b-114">No se admiten los conjuntos de propiedades que contiene las cadenas con nombre.</span><span class="sxs-lookup"><span data-stu-id="acf0b-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="acf0b-115">El formato de la sección **[extensión]** es:</span><span class="sxs-lookup"><span data-stu-id="acf0b-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="acf0b-116">**[Extensión.**</span><span class="sxs-lookup"><span data-stu-id="acf0b-116">**[Extension.**</span></span> <span data-ttu-id="acf0b-117">_cadena2_ **]**</span><span class="sxs-lookup"><span data-stu-id="acf0b-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="acf0b-118">**Tipo de** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="acf0b-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="acf0b-119">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="acf0b-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="acf0b-120">**NmidInteger** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="acf0b-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="acf0b-121">**Valor** =  _cadena_ |  _entero_</span><span class="sxs-lookup"><span data-stu-id="acf0b-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="acf0b-122">Se muestra un ejemplo de una sección **[Extensions]** y una sección posterior relacionada siguientes.</span><span class="sxs-lookup"><span data-stu-id="acf0b-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


