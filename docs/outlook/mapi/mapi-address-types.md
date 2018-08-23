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
ms.openlocfilehash: 80e933f5723746dbaeb39271cc813eb0ea56a705
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571188"
---
# <a name="mapi-address-types"></a>Tipos de direcciones MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todos los usuarios de mensajería está asociado con un tipo de dirección, una cadena de caracteres que describe el formato de la dirección del usuario que se almacena en la propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)). Tipos de direcciones que se asignan a formatos de dirección. Es decir, mirando en el tipo de dirección de un destinatario, las aplicaciones cliente pueden determinar cómo dar formato a una dirección apropiada para el destinatario. 
  
Por ejemplo, el `SMTP` tipo de dirección especifica la dirección de Internet estándar: 
  
 `username@companyname.com.`
  
Y, el `EX` tipo de dirección especifica una dirección de servidor de Exchange. 
  
Todas las entradas de la libreta de direcciones deben tener un tipo de dirección válida. Los clientes requieren que sus usuarios especificar un tipo de dirección al crear un tipo de destinatario personalizado no compatible con el proveedor de la libreta de direcciones. Para las entradas que admiten, se requieren los proveedores de la libreta de direcciones para proporcionar tipos de direcciones válidas. 
  
MAPI define el tipo de una sola dirección: MAPIPDL, que significa de lista de distribución personal.
  
Para obtener una lista de los tipos de direcciones compatibles con todos los proveedores de transporte en la sesión, las aplicaciones cliente de llaman al método **IMAPISession:: EnumAdrTypes** . Para obtener más información, vea [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).
  

