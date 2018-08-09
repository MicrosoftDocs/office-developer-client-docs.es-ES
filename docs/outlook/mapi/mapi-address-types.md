---
title: Tipos de direcciones MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 20eb429b2574f67e8b28ae96eeb96f42840123d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818066"
---
# <a name="mapi-address-types"></a>Tipos de direcciones MAPI

  
  
**Hace referencia a**: Outlook 
  
Todos los usuarios de mensajería está asociado con un tipo de dirección, una cadena de caracteres que describe el formato de la dirección del usuario que se almacena en la propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)). Tipos de direcciones que se asignan a formatos de dirección. Es decir, mirando en el tipo de dirección de un destinatario, las aplicaciones cliente pueden determinar cómo dar formato a una dirección apropiada para el destinatario. 
  
Por ejemplo, el `SMTP` tipo de dirección especifica la dirección de Internet estándar: 
  
 `username@companyname.com.`
  
Y, el `EX` tipo de dirección especifica una dirección de servidor de Exchange. 
  
Todas las entradas de la libreta de direcciones deben tener un tipo de dirección válida. Los clientes requieren que sus usuarios especificar un tipo de dirección al crear un tipo de destinatario personalizado no compatible con el proveedor de la libreta de direcciones. Para las entradas que admiten, se requieren los proveedores de la libreta de direcciones para proporcionar tipos de direcciones válidas. 
  
MAPI define el tipo de una sola dirección: MAPIPDL, que significa de lista de distribución personal.
  
Para obtener una lista de los tipos de direcciones compatibles con todos los proveedores de transporte en la sesión, las aplicaciones cliente de llaman al método **IMAPISession:: EnumAdrTypes** . Para obtener más información, vea [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).
  

