---
title: Recuperación de propiedades del destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a7bdcf133b8b2b5d8eb906cc0f5b5803838e27a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820516"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="858e3-103">Recuperación de propiedades del destinatario</span><span class="sxs-lookup"><span data-stu-id="858e3-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="858e3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="858e3-104">**Applies to**: Outlook</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="858e3-105">Para obtener acceso a una o varias propiedades de una entrada de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="858e3-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="858e3-106">Para cada entrada de la libreta de direcciones de interés, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md), pasando el identificador de entrada de usuario o lista de distribución de mensajería de destino.</span><span class="sxs-lookup"><span data-stu-id="858e3-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="858e3-107">A continuación, realice una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="858e3-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="858e3-108">El usuario de mensajería o método [IMAPIProp::GetProps](imapiprop-getprops.md) de la lista de distribución de llamadas para cada entrada de la libreta de direcciones de interés, con una lista de las propiedades de uno o más para recuperar.</span><span class="sxs-lookup"><span data-stu-id="858e3-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="858e3-109">Llame a [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), pasando una estructura [ADRLIST](adrlist.md) que contiene todas las propiedades de todas las entradas de la libreta de direcciones que desee.</span><span class="sxs-lookup"><span data-stu-id="858e3-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="858e3-110">Debido a que una llamada a **PrepareRecips** puede devolver información de dirección de varias entradas de la libreta, es la estrategia preferible cuando está interesado en más de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="858e3-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

