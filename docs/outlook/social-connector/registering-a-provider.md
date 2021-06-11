---
title: Registrar un proveedor
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: En este tema se describen las Windows de registro que se usan al instalar un proveedor Outlook Social Connector (OSC).
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421763"
---
# <a name="registering-a-provider"></a>Registrar un proveedor

En este tema se describen las Windows de registro que se usan al instalar un proveedor Outlook Social Connector (OSC).
  
## <a name="com-registration"></a>Registro COM

Debe configurar la DLL del proveedor de OSC para que se registre con el autoinscripción COM o regsvr32 durante la instalación. El registro COM de la DLL del proveedor registra el proveedor de OSC en el `HKEY_CLASSES_ROOT` subárbol del Registro. 
  
Un proveedor de OSC desarrollado en código administrado tiene un ensamblado de proveedor visible para COM. Debe usar un dominio de aplicación independiente para el componente de proveedor. De lo contrario, el proveedor de OSC usa el dominio de aplicación compartido predeterminado que usan otros componentes y es posible que el proveedor no funcione como se esperaba.
  
## <a name="registering-provider-progid"></a>ProgID del proveedor de registro

Cada proveedor de OSC debe registrar un identificador de programación ( `ProgID` ). El instalador del proveedor puede elegir una de las siguientes ubicaciones para agregar o quitar `ProgID` :
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;El instalador del proveedor debe usar esta ubicación si el proveedor está instalado solo para el usuario que ha iniciado sesión actualmente.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;El instalador del proveedor debe usar esta ubicación si el proveedor está instalado para todos los usuarios del equipo.
    
El OSC busca al proveedor en las ubicaciones anteriores, a menos que el equipo cliente tenga un Outlook de 32 bits en un sistema operativo de `ProgID` 64 Windows bits. En tal caso, el instalador del proveedor debe elegir una de las siguientes ubicaciones en el  `HKEY_CURRENT_USER`  `HKEY_LOCAL_MACHINE` subárbol or: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Para una versión hacer clic y ejecutar de Office, el instalador del proveedor debe elegir una de las siguientes ubicaciones en el subárbol HKEY_CURRENT_USER o HKEY_LOCAL_MACHINE siguiente:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Vea también

- [Lista de comprobación de instalación](installation-checklist.md)
- [Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implementación de un proveedor](deploying-a-provider.md)

