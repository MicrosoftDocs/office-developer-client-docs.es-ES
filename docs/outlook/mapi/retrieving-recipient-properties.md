---
title: Recuperación de propiedades del destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: a7bdcf133b8b2b5d8eb906cc0f5b5803838e27a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820516"
---
# <a name="retrieving-recipient-properties"></a>Recuperación de propiedades del destinatario
  
**Se aplica a**: Outlook 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Para obtener acceso a una o varias propiedades de una entrada de la libreta de direcciones
  
1. Para cada entrada de la libreta de direcciones de interés, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md), pasando el identificador de entrada de usuario o lista de distribución de mensajería de destino.
    
2. A continuación, realice una de las siguientes opciones:
    
   - El usuario de mensajería o método [IMAPIProp::GetProps](imapiprop-getprops.md) de la lista de distribución de llamadas para cada entrada de la libreta de direcciones de interés, con una lista de las propiedades de uno o más para recuperar. 
    
   - Llame a [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), pasando una estructura [ADRLIST](adrlist.md) que contiene todas las propiedades de todas las entradas de la libreta de direcciones que desee. Debido a que una llamada a **PrepareRecips** puede devolver información de dirección de varias entradas de la libreta, es la estrategia preferible cuando está interesado en más de un destinatario. 
    

