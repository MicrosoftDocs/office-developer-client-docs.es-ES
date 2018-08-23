---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 865d929f3348710b7786f4182670f3304a3a9244
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578041"
---
# <a name="attowner"></a><span data-ttu-id="feded-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="feded-103">attOwner</span></span>

  
  
<span data-ttu-id="feded-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="feded-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="feded-105">El atributo **attOwner** se codifica como cadenas contadas distribuyen to-end.</span><span class="sxs-lookup"><span data-stu-id="feded-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="feded-106">El formato de **attOwner** es como sigue:</span><span class="sxs-lookup"><span data-stu-id="feded-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="feded-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="feded-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="feded-108">longitud del nombre para mostrar de nombre para mostrar dirección longitud _dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="feded-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="feded-109">_dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="feded-109">_email-address_</span></span>
  
> <span data-ttu-id="feded-110">dirección de tipo **:**</span><span class="sxs-lookup"><span data-stu-id="feded-110">type **:** address</span></span> 
    
<span data-ttu-id="feded-111">A diferencia de otra longitud valores, la longitud del nombre para mostrar y la longitud de dirección son valores de 16 bits sin signo en lugar de enteros largos sin signo.</span><span class="sxs-lookup"><span data-stu-id="feded-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="feded-112">Aún incluyen terminar caracteres null, sin embargo.</span><span class="sxs-lookup"><span data-stu-id="feded-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="feded-113">Las cadenas de tipo y la dirección en la entrada de _dirección de correo electrónico_ están separadas por un carácter de dos puntos (:) literal, como "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="feded-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="feded-114">Sólo la cadena de dirección combinada del tipo **:** está terminada en null.</span><span class="sxs-lookup"><span data-stu-id="feded-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="feded-115">La asignación de las propiedades MAPI para el atributo **attOwner** depende de la clase de mensaje del mensaje que se va a codificar.</span><span class="sxs-lookup"><span data-stu-id="feded-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

