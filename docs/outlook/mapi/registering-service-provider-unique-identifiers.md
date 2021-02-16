---
title: Registro de identificadores únicos del proveedor de servicios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410178"
---
# <a name="registering-service-provider-unique-identifiers"></a>Registro de identificadores únicos del proveedor de servicios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La libreta de direcciones, el almacén de mensajes y los proveedores de transporte usan un identificador único conocido como [MAPIUID](mapiuid.md) para registrarse en objetos de servicio de varios tipos. Un **MAPIUID** es un identificador de 16 bytes que contiene un GUID. Puede crear un **MAPIUID** mediante el siguiente procedimiento: 
  
1. Definir una constante.
    
2. Invoque la Visual Studio *Crear GUID** . 
    
Por ejemplo, un proveedor de libreta de direcciones puede incluir la siguiente constante en un archivo de encabezado para definir **un MAPIUID:**
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **Para registrar un MAPIUID si su proveedor es un proveedor de libreta de direcciones o almacén de mensajes**
  
1. Llame [a IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
    
2. Registre un **MAPIUID** para cada objeto de inicio de sesión del que cree una instancia e incluya **este MAPIUID** en los primeros 16 bytes del miembro **ab** de cada identificador de entrada que cree. MAPI usa **estructuras MAPIUID** para asociar objetos con proveedores de servicios. Cuando un cliente llama al método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir un objeto, MAPI examina la parte **MAPIUID** del identificador de entrada, que coincide con el **MAPIUID** registrado, para determinar qué objeto de inicio de sesión debe recibir la solicitud abierta.
    
3. Si el proveedor es un transporte, registre una o más estructuras **MAPIUID** cuando MAPI llame al método **IXPLogon::AddressTypes.** MAPI usa las **estructuras MAPIUID registradas** por los proveedores de transporte para asignar la responsabilidad de la entrega de mensajes. 
    
Aunque los proveedores de servicios suelen registrar un **único MAPIUID,** puede registrar varias **estructuras MAPIUID.** Si su proveedor de libreta de direcciones o almacén de mensajes admite varios objetos de inicio de sesión, quizás al permitir que un usuario agregue más de una instancia del proveedor a su perfil, es posible que desee implementar un **MAPIUID** diferente para cada objeto de inicio de sesión. Existen otras razones para admitir más de un **MAPIUID:**
  
- Debe admitir más de una versión del proveedor y los identificadores de entrada deben representar la versión adecuada. Asignar un **MAPIUID diferente** para cada versión. 
    
- Desea distinguir entre los tipos de objetos que admite. Por ejemplo, es posible que un proveedor de libreta de direcciones desee registrar un **MAPIUID** para usarlo en los identificadores de entrada de sus objetos de usuario de mensajería y un **MAPIUID** diferente para usar para listas de distribución. 
    
Cuando hay varios objetos de inicio de sesión que están activos simultáneamente, tiene sentido tener estructuras **MAPIUID** únicas para cada uno. Esto aumenta la precisión con la que MAPI coincide con los identificadores de entrada de los proveedores de servicios y ahorra trabajo. Cuando cada objeto de inicio de sesión tiene su propio identificador único, MAPI puede garantizar que cualquier solicitud que enruta a un objeto de inicio de sesión puede ser manejada por ese objeto. Cuando los objetos de inicio de sesión comparten estructuras **MAPIUID,** MAPI enruta la solicitud al primer objeto de inicio de sesión identificado por **MAPIUID**. Si uno de los objetos de inicio de sesión recibe una solicitud que no puede procesar porque no controla el identificador de entrada, pase la solicitud al siguiente objeto de inicio de sesión antes de devolver un error.
  
## <a name="see-also"></a>Consulte también



[Implementación del inicio de sesión del proveedor de servicios](implementing-service-provider-logon.md)

