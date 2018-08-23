---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b292e65ddabcbe052832687a3dcf01658de5e379
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567478"
---
# <a name="attsentfor"></a><span data-ttu-id="6fd80-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="6fd80-103">attSentFor</span></span>

  
  
<span data-ttu-id="6fd80-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fd80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fd80-105">El atributo **attSentFor** se codifica como cadenas contadas distribuyen to-end.</span><span class="sxs-lookup"><span data-stu-id="6fd80-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="6fd80-106">El formato de **attSentFor** es como sigue:</span><span class="sxs-lookup"><span data-stu-id="6fd80-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="6fd80-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="6fd80-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="6fd80-108">longitud del nombre para mostrar de nombre para mostrar dirección longitud _dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="6fd80-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="6fd80-109">_dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="6fd80-109">_email-address_</span></span>
  
> <span data-ttu-id="6fd80-110">dirección de tipo **:**</span><span class="sxs-lookup"><span data-stu-id="6fd80-110">type **:** address</span></span> 
    
<span data-ttu-id="6fd80-111">A diferencia de otra longitud valores, la longitud del nombre para mostrar y la longitud de dirección son valores de 16 bits sin signo en lugar de enteros largos sin signo.</span><span class="sxs-lookup"><span data-stu-id="6fd80-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="6fd80-112">Aún incluyen terminar caracteres null, sin embargo.</span><span class="sxs-lookup"><span data-stu-id="6fd80-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="6fd80-113">Las cadenas de tipo y la dirección en la entrada de _dirección de correo electrónico_ están separadas por un carácter de dos puntos (:) literal, como "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="6fd80-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="6fd80-114">Sólo la cadena de dirección combinada del tipo **:** está terminada en null.</span><span class="sxs-lookup"><span data-stu-id="6fd80-114">Only the combined type **:** address string is null-terminated.</span></span>
  

