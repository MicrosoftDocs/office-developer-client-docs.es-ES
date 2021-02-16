---
title: Recuperar propiedades de los destinatarios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426677"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="f9f2f-103">Recuperar propiedades de los destinatarios</span><span class="sxs-lookup"><span data-stu-id="f9f2f-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="f9f2f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9f2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="f9f2f-105">Para obtener acceso a una o más propiedades de una entrada de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="f9f2f-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="f9f2f-106">Para cada entrada de interés de la libreta de direcciones, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md), pasando el identificador de entrada del usuario de mensajería de destino o la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="f9f2f-107">A continuación, realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="f9f2f-108">Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del usuario de mensajería o de la lista de distribución para cada entrada de interés de la libreta de direcciones, con una lista de las propiedades que se recuperarán.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="f9f2f-109">Llame [a IAddrBook::P repareRecips](iaddrbook-preparerecips.md)y pase una estructura [ADRLIST](adrlist.md) que contiene todas las propiedades de todas las entradas de la libreta de direcciones deseadas.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="f9f2f-110">Dado que una llamada a **PrepareRecips** puede devolver información para varias entradas de la libreta de direcciones, es la estrategia preferible cuando está interesado en más de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

