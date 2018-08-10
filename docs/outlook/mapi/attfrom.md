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
ms.openlocfilehash: c7c0d1df32a0ad6359fad20128a6a1e3dd225143
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816479"
---
# <a name="attfrom"></a><span data-ttu-id="1e8b4-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="1e8b4-103">attFrom</span></span>

<span data-ttu-id="1e8b4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e8b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e8b4-105">El atributo **attFrom** se codifica como una estructura **TRP** que codifica la dirección para mostrar, nombre y correo electrónico del remitente, seguido por el nombre para mostrar y la dirección del remitente, seguido de cualquier relleno es necesario.</span><span class="sxs-lookup"><span data-stu-id="1e8b4-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="1e8b4-106">El formato de **attFrom** es como sigue:</span><span class="sxs-lookup"><span data-stu-id="1e8b4-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="1e8b4-107">**attFrom**: relleno de _TRP estructura_ remitente-display-name _ dirección remitente _</span><span class="sxs-lookup"><span data-stu-id="1e8b4-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="1e8b4-108">El nombre para mostrar de remitente es una cadena terminada en null que se rellena con un carácter nulo adicional, si es necesario ponerse en contacto con un límite de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="1e8b4-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="1e8b4-109">El relleno al final de la codificación de **attFrom** consta de todos los caracteres null según sea necesario ponerse en contacto con un límite de **sizeof(TRP)** .</span><span class="sxs-lookup"><span data-stu-id="1e8b4-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="1e8b4-110">_TRP estructura:_ **trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="1e8b4-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="1e8b4-111">Para el elemento **attFrom** , el **TRP**-estructura es siempre un uso único de codificación, por lo que el trpid desactiva el **TRP**-campo de estructura es siempre **trpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="1e8b4-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="1e8b4-112">El cbgrtrp, cch y cb elementos corresponden a los campos restantes de la estructura **TRP** .</span><span class="sxs-lookup"><span data-stu-id="1e8b4-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="1e8b4-113">El campo cbgrtrp se calcula como la suma de **(sizeof(TRP) \*2)**, la longitud del terminada en null remitente--nombre para mostrar con su relleno y la longitud de la dirección de remitente terminada en null.</span><span class="sxs-lookup"><span data-stu-id="1e8b4-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="1e8b4-114">El campo cch se calcula como la longitud del nombre para mostrar de terminada en null con su relleno.</span><span class="sxs-lookup"><span data-stu-id="1e8b4-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="1e8b4-115">El campo cb se calcula como la longitud de la dirección de remitente terminada en null.</span><span class="sxs-lookup"><span data-stu-id="1e8b4-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="1e8b4-116">_dirección de remitente:_ **:** de tipo de dirección de direcciones **'\0'**</span><span class="sxs-lookup"><span data-stu-id="1e8b4-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="1e8b4-117">La dirección del remitente es una cadena que consta de cuatro partes, el tipo de dirección, un carácter literal de dos puntos (:), la propia dirección y un carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="1e8b4-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="1e8b4-118">Por ejemplo, la cadena `fax:1-909-555-1234\0` sería un valor legal de la dirección del remitente.</span><span class="sxs-lookup"><span data-stu-id="1e8b4-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  
