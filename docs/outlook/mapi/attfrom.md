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
# <a name="attfrom"></a><span data-ttu-id="b2261-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="b2261-103">attFrom</span></span>

<span data-ttu-id="b2261-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2261-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2261-105">El atributo **attFrom** se codifica como una estructura **TRP** que codifica el nombre para mostrar y la dirección de correo electrónico del remitente, seguido del nombre para mostrar y la dirección del remitente, seguido de cualquier relleno necesario.</span><span class="sxs-lookup"><span data-stu-id="b2261-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="b2261-106">El formato para **attFrom** es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="b2261-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="b2261-107">**attFrom**: _TRP-Structure_ Sender-Display-Name _ Sender-Address _ padding</span><span class="sxs-lookup"><span data-stu-id="b2261-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="b2261-108">Sender-Display-Name es una cadena terminada en null que se rellena con un carácter null adicional, si es necesario, para alcanzar un límite de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="b2261-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="b2261-109">El relleno al final de la codificación **attFrom** consta de todos los caracteres nulos que se necesitan para alcanzar un límite **sizeof (TRP)** .</span><span class="sxs-lookup"><span data-stu-id="b2261-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="b2261-110">_TRP-estructura:_ **trpidOneOff** cbgrtrp CCH CB</span><span class="sxs-lookup"><span data-stu-id="b2261-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="b2261-111">Para el elemento **attFrom** , la estructura **TRP**es siempre una codificación de uso único, por lo que la trpid fuera del campo de la estructura **TRP**es siempre **trpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="b2261-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="b2261-112">Los elementos cbgrtrp, CCH y CB corresponden a los demás campos de la estructura **TRP** .</span><span class="sxs-lookup"><span data-stu-id="b2261-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="b2261-113">El campo cbgrtrp se calcula como la suma de **(sizeof (TRP \*) 2)**, la longitud del Sender-Display-Name con su relleno y la longitud de la dirección de remitente-terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="b2261-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="b2261-114">El campo CCH se calcula como la longitud del nombre para mostrar terminada en NULL con su relleno.</span><span class="sxs-lookup"><span data-stu-id="b2261-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="b2261-115">El campo CB se calcula como la longitud de la dirección de remitente-terminada en nulo.</span><span class="sxs-lookup"><span data-stu-id="b2261-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="b2261-116">_Sender-Address:_ Dirección-tipo **:** dirección **' \ 0 '**</span><span class="sxs-lookup"><span data-stu-id="b2261-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="b2261-117">La dirección del remitente es una cadena compuesta por cuatro partes, el tipo de dirección, un literal de dos puntos (:), la propia dirección y un carácter null de terminación.</span><span class="sxs-lookup"><span data-stu-id="b2261-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="b2261-118">Por ejemplo, la cadena `fax:1-909-555-1234\0` sería un valor de remitente-dirección válido.</span><span class="sxs-lookup"><span data-stu-id="b2261-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

