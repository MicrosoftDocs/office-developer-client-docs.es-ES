---
title: Establecer el orden de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6e4c318678fdce7976140ff8f480ae638fd3ca4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593028"
---
# <a name="setting-transport-order"></a>Establecer el orden de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La cola MAPI asigna la responsabilidad de los mensajes salientes en función de los tipos de direcciones y los identificadores que los proveedores de transporte declaran que pueden controlar. Los proveedores de transporte publican una lista de tipos de direcciones compatibles y los identificadores — almacenados en las estructuras **MAPIUID** — cuando llama a su método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , MAPI directamente después de inicio de sesión. Tipo de dirección de un destinatario se almacena en su propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
Registrarse para un tipo de dirección indica a MAPI que el proveedor de transporte puede entregar a los destinatarios con la propiedad **PR_ADDRTYPE** establecida en el tipo de dirección registrados. De forma similar, registrar para un **MAPIUID** indica que el proveedor de transporte puede ofrecer a los destinatarios que están representados por los identificadores de entrada con el registrado **MAPIUID**.
  
Registrar la mayoría de los proveedores de transporte para uno o varios tipos de direcciones; pocos registrar por **MAPIUID**. Pueden registrar los proveedores de transporte que estén asociados estrechamente con un proveedor de la libreta de direcciones y comprender su formato de identificador de entrada para administrar los mensajes por **MAPIUID**, lo que mejora el rendimiento. Estos proveedores de transporte acoplado pueden extraer dirección de correo electrónico del destinatario y otra información necesaria desde el identificador de entrada sin tener que abrir con una llamada **IMAPISupport::OpenEntry** . 
  
MAPI mantiene una orden para los proveedores de transporte, usado cuando se hayan registrado varios proveedores de transporte para el mismo tipo de dirección o **MAPIUID**. Puede invalidar este orden mediante una llamada a [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) y pasando una lista ordenada de la s **MAPIUID**de todos los proveedores de transporte activo indicada por el parámetro _lpUIDList_ .: 
  
Para recuperar una lista de todos los tipos de direcciones que se pueden controlar mediante uno de los proveedores de transporte activo, llamar [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md). **EnumAdrTypes** devuelve una matriz de cadenas que describe los tipos de direcciones compatibles con los proveedores de transporte que están activos en la sesión actual. 
  

