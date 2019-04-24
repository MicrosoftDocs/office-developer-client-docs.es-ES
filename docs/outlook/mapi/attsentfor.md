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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318119"
---
# <a name="attsentfor"></a><span data-ttu-id="c513b-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="c513b-103">attSentFor</span></span>

  
  
<span data-ttu-id="c513b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c513b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c513b-105">El atributo **attSentFor** está codificado como cadenas contadas contenidas en un extremo a otro.</span><span class="sxs-lookup"><span data-stu-id="c513b-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="c513b-106">El formato para **attSentFor** es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="c513b-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="c513b-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="c513b-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="c513b-108">Display-Name-length nombre-longitud de dirección dirección de _correo electrónico-dirección_</span><span class="sxs-lookup"><span data-stu-id="c513b-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="c513b-109">_Dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="c513b-109">_email-address_</span></span>
  
> <span data-ttu-id="c513b-110">tipo **:** Address</span><span class="sxs-lookup"><span data-stu-id="c513b-110">type **:** address</span></span> 
    
<span data-ttu-id="c513b-111">A diferencia de otros valores de longitud, Display-Name-length and Address-length son valores de 16 bits sin signo en lugar de enteros largos sin signo.</span><span class="sxs-lookup"><span data-stu-id="c513b-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="c513b-112">Sin embargo, aún incluyen el final de los caracteres nulos.</span><span class="sxs-lookup"><span data-stu-id="c513b-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="c513b-113">Las cadenas de tipo y dirección de la entrada de _dirección de correo electrónico_ están separadas por dos puntos literales (:) carácter, como "SMTP:Joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="c513b-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="c513b-114">Solo el tipo combinado **:** la cadena de dirección termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="c513b-114">Only the combined type **:** address string is null-terminated.</span></span>
  

