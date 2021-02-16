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
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433601"
---
# <a name="setting-transport-order"></a>Establecer el orden de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La cola MAPI asigna la responsabilidad de los mensajes salientes en función de los tipos de direcciones e identificadores que los proveedores de transporte declaran que pueden controlar. Los proveedores de transporte publican una lista de identificadores y tipos de direcciones admitidos (almacenados en estructuras **MAPIUID)** cuando MAPI llama a su método [IXPLogon::AddressTypes,](ixplogon-addresstypes.md) directamente después del inicio de sesión. El tipo de dirección de un destinatario se almacena en **su PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
El registro de un tipo de dirección indica a MAPI que el proveedor de transporte puede entregar a los destinatarios con su propiedad **PR_ADDRTYPE** establecida en el tipo de dirección registrada. De forma similar, el registro de **un MAPIUID** indica que el proveedor de transporte puede entregar a los destinatarios representados por identificadores de entrada con el **MAPIUID registrado.**
  
La mayoría de los proveedores de transporte se registran para uno o más tipos de direcciones; pocos registrados **por MAPIUID**. Los proveedores de transporte estrechamente asociados con un proveedor de libreta de direcciones y que comprenden su formato de identificador de entrada pueden registrarse para controlar los mensajes mediante **MAPIUID,** lo que mejora el rendimiento. Estos proveedores de transporte estrechamente acoplados pueden extraer la dirección de correo electrónico del destinatario y otra información necesaria del identificador de entrada sin tener que abrirlo con una llamada **IMAPISupport::OpenEntry.** 
  
MAPI mantiene un orden para los proveedores de transporte, que se usa cuando varios proveedores de transporte se han registrado para el mismo tipo de dirección o **MAPIUID**. Puede invalidar este orden llamando a [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) y pasando una lista ordenada de **los MAPIUID** de todos los proveedores de transporte activos a los que apunta el parámetro _lpUIDList:_ 
  
Para recuperar una lista de todos los tipos de direcciones que puede controlar uno de los proveedores de transporte activos, llame a [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md). **EnumAdrTypes** devuelve una matriz de cadenas que describe los tipos de dirección admitidos por los proveedores de transporte que están activos en la sesión actual. 
  

