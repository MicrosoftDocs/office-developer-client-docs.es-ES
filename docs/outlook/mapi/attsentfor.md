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
ms.openlocfilehash: fd7f79ad7a36fd174bf9817ff463b00e6a334104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816493"
---
# <a name="attsentfor"></a><span data-ttu-id="269f3-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="269f3-103">attSentFor</span></span>

  
  
<span data-ttu-id="269f3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="269f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="269f3-105">El atributo **attSentFor** se codifica como cadenas contadas distribuyen to-end.</span><span class="sxs-lookup"><span data-stu-id="269f3-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="269f3-106">El formato de **attSentFor** es como sigue:</span><span class="sxs-lookup"><span data-stu-id="269f3-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="269f3-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="269f3-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="269f3-108">longitud del nombre para mostrar de nombre para mostrar dirección longitud _dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="269f3-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="269f3-109">_dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="269f3-109">_email-address_</span></span>
  
> <span data-ttu-id="269f3-110">dirección de tipo **:**</span><span class="sxs-lookup"><span data-stu-id="269f3-110">type **:** address</span></span> 
    
<span data-ttu-id="269f3-111">A diferencia de otra longitud valores, la longitud del nombre para mostrar y la longitud de dirección son valores de 16 bits sin signo en lugar de enteros largos sin signo.</span><span class="sxs-lookup"><span data-stu-id="269f3-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="269f3-112">Aún incluyen terminar caracteres null, sin embargo.</span><span class="sxs-lookup"><span data-stu-id="269f3-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="269f3-113">Las cadenas de tipo y la dirección en la entrada de _dirección de correo electrónico_ están separadas por un carácter de dos puntos (:) literal, como "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="269f3-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="269f3-114">Sólo la cadena de dirección combinada del tipo **:** está terminada en null.</span><span class="sxs-lookup"><span data-stu-id="269f3-114">Only the combined type **:** address string is null-terminated.</span></span>
  

