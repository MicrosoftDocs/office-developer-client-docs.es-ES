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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405439"
---
# <a name="mapi-address-types"></a>Tipos de direcciones MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cada usuario de mensajería está asociado con un tipo de dirección, una cadena de caracteres que describe el formato de la dirección del usuario que se almacena en la propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)). Los tipos de direcciones se asignan a formatos de dirección. Es decir, al ver el tipo de dirección de un destinatario, las aplicaciones cliente pueden determinar cómo dar formato a una dirección adecuada para el destinatario. 
  
Por ejemplo, el  `SMTP` tipo de dirección especifica la dirección de Internet estándar: 
  
 `username@companyname.com.`
  
Además, el `EX` tipo de dirección especifica una Exchange Server dirección. 
  
Todas las entradas de la libreta de direcciones deben tener un tipo de dirección válido. Los clientes requieren que sus usuarios especifiquen un tipo de dirección al crear un tipo de destinatario personalizado no admitido por el proveedor de libreta de direcciones. Para las entradas que admiten, los proveedores de libreta de direcciones deben proporcionar tipos de direcciones válidos. 
  
MAPI define solo un tipo de dirección: MAPIPDL, que significa lista de distribución personal.
  
Para obtener una lista de los tipos de direcciones admitidos por todos los proveedores de transporte de la sesión, las aplicaciones cliente llaman al método **IMAPISession::EnumAdrTypes.** Para obtener más información, [vea IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).
  

