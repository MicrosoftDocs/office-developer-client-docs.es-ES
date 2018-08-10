---
title: Registrar un proveedor
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: En este tema se describe las ubicaciones del registro de Windows que se usan cuando se instala un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821206"
---
# <a name="registering-a-provider"></a>Registrar un proveedor

En este tema se describe las ubicaciones del registro de Windows que se usan cuando se instala un proveedor de Outlook Social Connector (OSC).
  
## <a name="com-registration"></a>Registro COM

Debe configurar el proveedor de OSC DLL para registrar el uso de registro automático de COM o regsvr32 durante la instalación. Registro de COM de la DLL del proveedor registra el proveedor de OSC bajo la `HKEY_CLASSES_ROOT` subárbol del registro. 
  
Un proveedor de OSC desarrollado en código administrado tiene un ensamblado COM-visible del proveedor. Debe usar un dominio de aplicación independiente para el componente de proveedor. De lo contrario, el proveedor de OSC usa el dominio de aplicación compartida predeterminada que se usa en otros componentes, y el proveedor no funcionen según lo previsto.
  
## <a name="registering-provider-progid"></a>Registrar proveedor ProgID

Cada proveedor de OSC debe registrar un identificador de programación (`ProgID`). El instalador de proveedor puede elegir una de las siguientes ubicaciones para agregar o quitar el `ProgID`:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Al instalador del proveedor debe usar esta ubicación si el proveedor está instalado para sólo el usuario que inició sesión actualmente.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Al instalador del proveedor debe usar esta ubicación si el proveedor está instalado para todos los usuarios en el equipo.
    
Busca el OSC para el proveedor de `ProgID` en las ubicaciones anteriores, a menos que el equipo cliente tenga Outlook de 32 bits que se ejecutan en un sistema operativo de Windows de 64 bits. En tal caso, el instalador de proveedor debe elegir una de las siguientes ubicaciones en la `HKEY_CURRENT_USER` o `HKEY_LOCAL_MACHINE` subárbol: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Para obtener una versión de hacer clic y ejecutar de Office, el instalador de proveedor debe elegir una de las siguientes ubicaciones en el subárbol HKEY_CURRENT_USER o HKEY_LOCAL_MACHINE:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Vea también

- [Lista de comprobación de instalación](installation-checklist.md)
- [Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implementación de un proveedor](deploying-a-provider.md)

