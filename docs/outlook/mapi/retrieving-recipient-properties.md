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
# <a name="retrieving-recipient-properties"></a>Recuperar propiedades de los destinatarios
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Para obtener acceso a una o más propiedades de una entrada de libreta de direcciones
  
1. Para cada entrada de la libreta de direcciones de interés, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md), pasando el identificador de entrada del usuario de mensajería de destino o la lista de distribución.
    
2. A continuación, realice una de las siguientes acciones:
    
   - Llama al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la lista de mensajería para cada entrada de interés de la libreta de direcciones, con una lista de las propiedades que se recuperarán. 
    
   - Llame [a IAddrBook::P repareRecips](iaddrbook-preparerecips.md), pasando una estructura [ADRLIST](adrlist.md) que contiene todas las propiedades de todas las entradas de la libreta de direcciones deseadas. Dado que una llamada a **PrepareRecips** puede devolver información para varias entradas de libreta de direcciones, es la estrategia preferible cuando está interesado en más de un destinatario. 
    

