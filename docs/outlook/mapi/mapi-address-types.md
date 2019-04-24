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
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298015"
---
# <a name="mapi-address-types"></a>Tipos de direcciones MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cada usuario de mensajería está asociado a un tipo de dirección, una cadena de caracteres que describe el formato de la dirección del usuario que se almacena en la propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)). Los tipos de direcciones se asignan a formatos de dirección. Es decir, al mirar el tipo de dirección de un destinatario, las aplicaciones cliente pueden determinar cómo dar formato a una dirección adecuada para el destinatario. 
  
Por ejemplo, el `SMTP` tipo de dirección especifica la dirección de Internet estándar: 
  
 `username@companyname.com.`
  
Y el `EX` tipo de dirección especifica una dirección del servidor de Exchange. 
  
Todas las entradas de la libreta de direcciones deben tener un tipo de dirección válida. Los clientes requieren que los usuarios especifiquen un tipo de dirección al crear un tipo de destinatario personalizado no admitido por el proveedor de la libreta de direcciones. Para las entradas que admiten, los proveedores de la libreta de direcciones deben suministrar tipos de direcciones válidos. 
  
MAPI define un solo tipo de dirección: MAPIPDL, que significa lista de distribución personal.
  
Para obtener una lista de los tipos de direcciones admitidos por todos los proveedores de transporte en la sesión, las aplicaciones cliente llaman al método **IMAPISession:: EnumAdrTypes** . Para obtener más información, vea [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).
  

