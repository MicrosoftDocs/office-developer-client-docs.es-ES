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
ms.openlocfilehash: a48c6a8e043062bc6b48e09934fded1dccb507b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585440"
---
# <a name="retrieving-recipient-properties"></a>Recuperación de propiedades del destinatario
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Para obtener acceso a una o varias propiedades de una entrada de la libreta de direcciones
  
1. Para cada entrada de la libreta de direcciones de interés, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md), pasando el identificador de entrada de usuario o lista de distribución de mensajería de destino.
    
2. A continuación, realice una de las siguientes opciones:
    
   - El usuario de mensajería o método [IMAPIProp::GetProps](imapiprop-getprops.md) de la lista de distribución de llamadas para cada entrada de la libreta de direcciones de interés, con una lista de las propiedades de uno o más para recuperar. 
    
   - Llame a [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), pasando una estructura [ADRLIST](adrlist.md) que contiene todas las propiedades de todas las entradas de la libreta de direcciones que desee. Debido a que una llamada a **PrepareRecips** puede devolver información de dirección de varias entradas de la libreta, es la estrategia preferible cuando está interesado en más de un destinatario. 
    

