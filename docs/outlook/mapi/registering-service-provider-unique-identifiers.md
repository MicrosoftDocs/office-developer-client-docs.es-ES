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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328402"
---
# <a name="registering-service-provider-unique-identifiers"></a>Registro de identificadores únicos del proveedor de servicios

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
La libreta de direcciones, el almacén de mensajes y los proveedores de transporte usan un identificador único conocido como [MAPIUID](mapiuid.md) para registrarse en objetos de servicio de distintos tipos. Un **MAPIUID** es un identificador de 16 bytes que contiene un GUID. Puede crear un **MAPIUID** mediante el siguiente procedimiento: 
  
1. Defina una constante.
    
2. Invocar la herramienta Visual Studio*Create GUID**. 
    
Por ejemplo, un proveedor de libreta de direcciones puede incluir la siguiente constante en un archivo de encabezado para definir un **MAPIUID**:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **Para registrar un MAPIUID si su proveedor es una libreta de direcciones o un proveedor de almacenamiento de mensajes**
  
1. Llamar a [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).
    
2. Registre un **MAPIUID** para cada objeto de inicio de sesión del que cree una instancia e incluya este **MAPIUID** en los primeros 16 bytes del miembro **AB** de cada identificador de entrada que cree. MAPI usa estructuras **MAPIUID** para asociar objetos con proveedores de servicios. Cuando un cliente llama al método [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir un objeto, MAPI examina la parte **MAPIUID** del identificador de la entrada, la compara con el **MAPIUID**registrado, para determinar qué objeto de inicio de sesión debe recibir la apertura solicitud.
    
3. Si su proveedor es un transporte, registre una o varias estructuras **MAPIUID** cuando MAPI llame a su método **IXPLogon:: AddressTypes** . MAPI usa las estructuras **MAPIUID** registradas por los proveedores de transporte para asignar responsabilidades para la entrega de mensajes. 
    
Aunque los proveedores de servicios normalmente registran una única **MAPIUID**, puede registrar varias estructuras de **MAPIUID** . Si la libreta de direcciones o el proveedor de almacenamiento de mensajes admite varios objetos de inicio de sesión, por ejemplo, si se permite que un usuario agregue más de una instancia de su proveedor a su perfil, es posible que desee implementar una **MAPIUID** diferente para cada objeto de inicio de sesión. Hay otras razones para admitir más de un **MAPIUID**:
  
- Debe admitir más de una versión de su proveedor y los identificadores de entrada deben representar la versión adecuada. Asigne un **MAPIUID** diferente para cada versión. 
    
- Desea distinguir entre los tipos de objetos que admite. Por ejemplo, es posible que un proveedor de libreta de direcciones desee registrar una **MAPIUID** para usarla en los identificadores de entrada de sus objetos de usuario de mensajería y un **MAPIUID** diferente para usarla para las listas de distribución. 
    
Cuando hay varios objetos de inicio de sesión que están activos simultáneamente, es lógico tener estructuras **MAPIUID** únicas para cada uno. Esto aumenta la precisión con la que MAPI hace coincidir los identificadores de entrada con los proveedores de servicios y guarda algún trabajo. Cuando cada objeto de inicio de sesión tiene su propio identificador único, MAPI puede garantizar que cualquier solicitud que se dirige a un objeto de inicio de sesión puede controlarse con ese objeto. Cuando los objetos de inicio de sesión comparten estructuras **MAPIUID** , MAPI enruta la solicitud al primer objeto de inicio de sesión identificado por el **MAPIUID**. Si uno de los objetos de inicio de sesión recibe una solicitud que no puede procesar porque no controla el identificador de entrada, pase la solicitud al siguiente objeto de inicio de sesión antes de devolver un error.
  
## <a name="see-also"></a>Vea también



[Implementar el inicio de sesión del proveedor de servicios](implementing-service-provider-logon.md)

