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
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427657"
---
# <a name="attowner"></a><span data-ttu-id="b716a-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="b716a-103">attOwner</span></span>

  
  
<span data-ttu-id="b716a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b716a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b716a-105">El **atributo attOwner** se codifica como cadenas contadas establecidas de un extremo a otro.</span><span class="sxs-lookup"><span data-stu-id="b716a-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="b716a-106">El formato de **attOwner** es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="b716a-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="b716a-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="b716a-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="b716a-108">display-name-length display-name address-length  _email-address_</span><span class="sxs-lookup"><span data-stu-id="b716a-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="b716a-109">_email-address_</span><span class="sxs-lookup"><span data-stu-id="b716a-109">_email-address_</span></span>
  
> <span data-ttu-id="b716a-110">tipo **:** address</span><span class="sxs-lookup"><span data-stu-id="b716a-110">type **:** address</span></span> 
    
<span data-ttu-id="b716a-111">A diferencia de otros valores de longitud, los valores para mostrar-name-length y address-length son valores de 16 bits sin signo en lugar de enteros largos sin signo.</span><span class="sxs-lookup"><span data-stu-id="b716a-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="b716a-112">Sin embargo, aún incluyen los caracteres nulos de terminación.</span><span class="sxs-lookup"><span data-stu-id="b716a-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="b716a-113">Las cadenas de tipo y dirección de la entrada  _de dirección de_ correo electrónico están separadas por dos puntos literales (:) carácter, como "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="b716a-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="b716a-114">Solo el tipo combinado **:** la cadena de dirección termina en null.</span><span class="sxs-lookup"><span data-stu-id="b716a-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="b716a-115">La asignación de propiedades MAPI al **atributo attOwner** depende de la clase de mensaje del mensaje que se codifica.</span><span class="sxs-lookup"><span data-stu-id="b716a-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

