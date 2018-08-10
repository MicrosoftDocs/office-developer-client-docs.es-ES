---
title: Registrar identificadores únicos del proveedor de servicios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 80d2e4fd353f0746349563fd911e0af09a658b35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820491"
---
# <a name="registering-service-provider-unique-identifiers"></a>Registrar identificadores únicos del proveedor de servicios

  
  
**Hace referencia a**: Outlook 
  
Libreta de direcciones, almacén de mensajes y los proveedores de transporte utilizan un identificador único conocido como un [MAPIUID](mapiuid.md) para registrar a los objetos de servicio de diversos tipos. Un **MAPIUID** es un identificador de 16 bytes que contiene un GUID. Puede crear un **MAPIUID** mediante el siguiente procedimiento: 
  
1. Definir una constante.
    
2. Invocar el Visual Studio*Crear GUID** herramienta. 
    
Por ejemplo, un proveedor de la libreta de direcciones puede incluir la siguiente constante en un archivo de encabezado para definir una **MAPIUID**:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **Para registrar un MAPIUID si su proveedor es un proveedor de almacén de mensaje o de la libreta de direcciones**
  
1. Llame a [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
    
2. Registrar un **MAPIUID** para cada inicio de sesión de objetos que crear una instancia e incluir este **MAPIUID** en los primeros 16 bytes del miembro **ab** de cada identificador de entrada que cree. MAPI utiliza estructuras **MAPIUID** para asociar objetos con proveedores de servicios. Cuando un cliente llama el método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir un objeto, MAPI examina la parte **MAPIUID** del identificador de entrada, que coincida con el registrado **MAPIUID**, para determinar qué objeto de inicio de sesión debe recibir el abrir solicitud.
    
3. Si su proveedor es un transporte, registrar una o más estructuras **MAPIUID** cuando MAPI llama al método **IXPLogon::AddressTypes** . MAPI utiliza las estructuras **MAPIUID** registradas por los proveedores de transporte para asignar la responsabilidad de la entrega del mensaje. 
    
Aunque los proveedores de servicios suele registran un único **MAPIUID**, se pueden registrar varios estructuras **MAPIUID** . Si su libreta de direcciones o mensaje almacena proveedor admite varios objetos de inicio de sesión, quizás por lo que permite al usuario agregar más de una instancia de su proveedor a sus perfiles, es posible que desee implementar un diferentes **MAPIUID** para cada objeto de inicio de sesión. Hay algunas otras razones para admitir más de un **MAPIUID**:
  
- Debe admitir más de una versión de su proveedor y los identificadores de entrada deben representar la versión adecuada. Asignar un diferentes **MAPIUID** para cada versión. 
    
- Desea distinguir entre los tipos de objetos que admite. Por ejemplo, un proveedor de la libreta de direcciones es posible que desee registrar un **MAPIUID** para usar en los identificadores de entrada de sus objetos de usuario de mensajería y un diferentes **MAPIUID** que se usará para las listas de distribución. 
    
Cuando hay varios objetos de inicio de sesión que están activos simultáneamente, tiene sentido tienen estructuras **MAPIUID** únicas para cada uno de ellos. Esto aumenta la precisión con la que coincide con los identificadores de entrada a proveedores de servicios MAPI y guarda algún trabajo. Cuando todos los objetos de inicio de sesión tienen su propio identificador único, MAPI puede garantizar que cualquier solicitud rutas a un objeto de inicio de sesión pueden controlarse por dicho objeto. Cuando los objetos de inicio de sesión comparten estructuras **MAPIUID** , MAPI enruta la solicitud para el primer objeto de inicio de sesión que se identifica con el **MAPIUID**. Si uno de los objetos de inicio de sesión recibe una solicitud que no se puede procesar porque no controla el identificador de entrada, pase la solicitud de sesión en el siguiente objeto de inicio de sesión antes de devolver un error.
  
## <a name="see-also"></a>Vea también



[Implementar el inicio de sesión del proveedor de servicios](implementing-service-provider-logon.md)

