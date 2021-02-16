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
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408841"
---
# <a name="attsentfor"></a><span data-ttu-id="e669f-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="e669f-103">attSentFor</span></span>

  
  
<span data-ttu-id="e669f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e669f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e669f-105">El **atributo attSentFor** se codifica como cadenas contadas colocadas de un extremo a otro.</span><span class="sxs-lookup"><span data-stu-id="e669f-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="e669f-106">El formato de **attSentFor** es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="e669f-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="e669f-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="e669f-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="e669f-108">display-name-length display-name address-length  _email-address_</span><span class="sxs-lookup"><span data-stu-id="e669f-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="e669f-109">_email-address_</span><span class="sxs-lookup"><span data-stu-id="e669f-109">_email-address_</span></span>
  
> <span data-ttu-id="e669f-110">type **:** address</span><span class="sxs-lookup"><span data-stu-id="e669f-110">type **:** address</span></span> 
    
<span data-ttu-id="e669f-111">A diferencia de otros valores de longitud, la longitud del nombre para mostrar y la longitud de la dirección son valores de 16 bits sin signo en lugar de enteros largos sin signo.</span><span class="sxs-lookup"><span data-stu-id="e669f-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="e669f-112">Sin embargo, aún incluyen la terminación de caracteres nulos.</span><span class="sxs-lookup"><span data-stu-id="e669f-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="e669f-113">Las cadenas de tipo y dirección de la entrada  _de dirección_ de correo electrónico están separadas por dos puntos literales (:) como, por ejemplo, "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="e669f-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="e669f-114">Solo el tipo **combinado: la** cadena de dirección termina en null.</span><span class="sxs-lookup"><span data-stu-id="e669f-114">Only the combined type **:** address string is null-terminated.</span></span>
  

