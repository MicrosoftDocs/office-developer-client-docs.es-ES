---
title: Acceso delegado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 3d6a0eaf8ad125a0ae1ea3abb57e2aa57e0bdfe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427265"
---
# <a name="delegate-access"></a>Acceso delegado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Acceso delegado hace referencia a la capacidad del usuario para enviar un mensaje como otro usuario o recibir un mensaje de otro usuario. Acceso delegado es una caracter�stica independiente del proveedor de servicio de MAPI que admiten los proveedores de transporte si eligen. Sin embargo, ning�n proveedor es necesario para hacerlo. Acceso delegado es valioso cuando sea necesario para un usuario enviar mensajes como o filtrar los mensajes entrantes de otro usuario o al usuario debe tener acceso al almac�n de mensajes de otro usuario. Antes de permitir que un usuario delegado conectar al almac�n de otro usuario, el proveedor de almacenamiento de mensaje debe comprobar que el usuario delegado tiene la autoridad apropiada. 
  
Hay dos grupos de propiedades que se usan para admitir el acceso de delegado:
  
 **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md)) 
  
En los mensajes salientes, las propiedades de **PR_SENT_REPRESENTING** identifican al usuario de mensajer�a que debe actuar como el remitente. Los clientes pueden establecer estas propiedades como una opci�n. Si no se establecen las propiedades de **PR_SENT_REPRESENTING** con el tiempo el mensaje llega a un proveedor de transporte que admite el acceso delegado, es responsabilidad del proveedor para establecerlas junto con las propiedades de **PR_SENDER**. 
  
En los mensajes entrantes, las propiedades de **PR_RCVD_REPRESENTING** identifican al usuario que debe actuar como el destinatario. Los proveedores de transporte responsable de entregar los mensajes de delegado deben establecer las propiedades de los **PR_RCVD_REPRESENTING** y **PR_RECEIVED_BY**. Los clientes de recibir un mensaje de delegado deben copiar los valores de las propiedades **PR_SENT_REPRESENTING** a las propiedades de **PR_RCVD_REPRESENTING** correspondientes. 
  
Por ejemplo, suponga que John est� recibiendo mensajes de Mar�a mientras Mar�a est� de vacaciones. Las propiedades de **PR_RCVD_REPRESENTING** identifican John como el destinatario de delegado. Cuando Juan env�a una respuesta a un mensaje que ha recibido para Mar�a, las propiedades del mensaje **PR_SENDER** identifican John como el remitente. Debido a que John representa a Mar�a, las propiedades de **PR_SENT_REPRESENTING** identifican Mar�a. 
  
Los mensajes entrantes de delegado de tratamiento normalmente deben enviar estos mensajes como el usuario de mensajer�a identificado por las propiedades **PR_SENT_REPRESENTING** en lugar de como el usuario identificado por las propiedades de **PR_SENDER** los proveedores de transporte. La excepci�n a esta regla es cuando sea necesario para que coincida con los tipos de privilegio y transporte de access. En este caso, un proveedor de transporte puede elegir una identidad de env�a. 
  
Si las propiedades de **PR_SENT_REPRESENTING** est�n disponibles para un mensaje entrante de delegado, el proveedor de transporte controlar entrega debe establecer, con los valores de las propiedades correspondientes de **PR_SENDER**. Si las propiedades de **PR_SENT_REPRESENTING** est�n disponibles, pero el proveedor de transporte no admite el acceso de delegado, puede usar las propiedades de **PR_SENDER** para la entrega. 
  

