---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432418"
---
# <a name="attfrom"></a><span data-ttu-id="5f7e0-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="5f7e0-103">attFrom</span></span>

<span data-ttu-id="5f7e0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f7e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f7e0-105">El atributo **attFrom** se codifica como una estructura **TRP** que codifica el nombre para mostrar y la dirección de correo electrónico del remitente, seguido del nombre para mostrar y la dirección del remitente, seguido de cualquier espaciado interno necesario.</span><span class="sxs-lookup"><span data-stu-id="5f7e0-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="5f7e0-106">El formato de **attFrom** es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="5f7e0-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="5f7e0-107">**attFrom**: _TRP-structure_ sender-display-name _ sender-address _ padding</span><span class="sxs-lookup"><span data-stu-id="5f7e0-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="5f7e0-108">El nombre para mostrar del remitente es una cadena terminada en null que se agrega con un carácter nulo adicional, si es necesario, para alcanzar un límite de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="5f7e0-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="5f7e0-109">El relleno al final de la codificación **attFrom** consta de tantos caracteres nulos como sea necesario para alcanzar un **límite sizeof(TRP).**</span><span class="sxs-lookup"><span data-stu-id="5f7e0-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="5f7e0-110">_Estructura TRP:_ **trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="5f7e0-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="5f7e0-111">Para el **elemento attFrom,** **la TRP**-structure siempre es una codificación de uso único, por lo que el trpid off del campo **TRP**-structure siempre **es trpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="5f7e0-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="5f7e0-112">Los elementos cbgrtrp, cch y cb corresponden a los campos restantes de la **estructura TRP.**</span><span class="sxs-lookup"><span data-stu-id="5f7e0-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="5f7e0-113">El campo cbgrtrp se calcula como la suma de **(sizeof(TRP) \* 2),** la longitud del nombre para mostrar del remitente terminada en null con su relleno y la longitud de la dirección del remitente terminada en null.</span><span class="sxs-lookup"><span data-stu-id="5f7e0-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="5f7e0-114">El campo cch se calcula como la longitud del nombre para mostrar terminada en null con su relleno.</span><span class="sxs-lookup"><span data-stu-id="5f7e0-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="5f7e0-115">El campo cb se calcula como la longitud de la dirección del remitente terminada en null.</span><span class="sxs-lookup"><span data-stu-id="5f7e0-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="5f7e0-116">_sender-address:_ address-type **:** address **'\0'**</span><span class="sxs-lookup"><span data-stu-id="5f7e0-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="5f7e0-117">La dirección del remitente es una cadena compuesta por cuatro partes, el tipo de dirección, dos puntos literales (:), la propia dirección y un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="5f7e0-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="5f7e0-118">Por ejemplo, la cadena `fax:1-909-555-1234\0` sería un valor de dirección de remitente legal.</span><span class="sxs-lookup"><span data-stu-id="5f7e0-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

