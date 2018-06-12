---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 0cb40c3c644618bdf65a2c90a91580a5be8fc88c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816473"
---
# <a name="attowner"></a><span data-ttu-id="85fb5-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="85fb5-103">attOwner</span></span>

  
  
<span data-ttu-id="85fb5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85fb5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85fb5-105">El atributo **attOwner** se codifica como cadenas contadas distribuyen to-end.</span><span class="sxs-lookup"><span data-stu-id="85fb5-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="85fb5-106">El formato de **attOwner** es como sigue:</span><span class="sxs-lookup"><span data-stu-id="85fb5-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="85fb5-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="85fb5-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="85fb5-108">longitud del nombre para mostrar de nombre para mostrar dirección longitud _dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="85fb5-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="85fb5-109">_dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="85fb5-109">_email-address_</span></span>
  
> <span data-ttu-id="85fb5-110">dirección de tipo **:**</span><span class="sxs-lookup"><span data-stu-id="85fb5-110">type **:** address</span></span> 
    
<span data-ttu-id="85fb5-111">A diferencia de otra longitud valores, la longitud del nombre para mostrar y la longitud de dirección son valores de 16 bits sin signo en lugar de enteros largos sin signo.</span><span class="sxs-lookup"><span data-stu-id="85fb5-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="85fb5-112">Aún incluyen terminar caracteres null, sin embargo.</span><span class="sxs-lookup"><span data-stu-id="85fb5-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="85fb5-113">Las cadenas de tipo y la dirección en la entrada de _dirección de correo electrónico_ están separadas por un carácter de dos puntos (:) literal, como "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="85fb5-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="85fb5-114">Sólo la cadena de dirección combinada del tipo **:** está terminada en null.</span><span class="sxs-lookup"><span data-stu-id="85fb5-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="85fb5-115">La asignación de las propiedades MAPI para el atributo **attOwner** depende de la clase de mensaje del mensaje que se va a codificar.</span><span class="sxs-lookup"><span data-stu-id="85fb5-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

