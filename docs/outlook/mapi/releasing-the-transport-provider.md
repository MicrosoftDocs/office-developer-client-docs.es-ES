---
title: Liberar el proveedor de transporte
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328388"
---
# <a name="releasing-the-transport-provider"></a>Liberar el proveedor de transporte

 
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Cuando MAPI o la cola MAPI terminan de usar un objeto de inicio de sesión de transporte:
  
1. MAPI o la cola MAPI llama al método [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) del proveedor de transporte. 
    
2. El proveedor de transporte invalida el objeto de estado mediante una llamada al método [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) . Si el proveedor de transporte invalida los objetos de mensaje que se envían o reciben en el momento de la llamada **TransportLogoff** depende de las marcas que se pasaron a **TransportLogoff**.
    
3. El proveedor de transporte llama al método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del objeto de soporte para quitar la fila del proveedor de transporte de la tabla de estado y quitar de las tablas internas cualquier identificador único (UID) que se haya establecido con la [IMAPISupport:: Método SetProviderUID](imapisupport-setprovideruid.md) . Disminuye el número de objetos de inicio de sesión conocidos activos en este objeto de proveedor. Si el recuento llega a cero, MAPI llama al método [IXPProvider:: Shutdown](ixpprovider-shutdown.md) y **Release** en el objeto de proveedor. Si este era el último objeto de proveedor conocido que usa esta DLL en este proceso, MAPI llama a la función **FreeLibrary** en el dll en un momento posterior. Se libera la memoria para el objeto compatibilidad con MAPI y se devuelve el método support Object **Release** . 
    
4. El método **TransportLogoff** Devuelve S_OK. 
    
5. MAPI o la cola MAPI llama a **Release** en el objeto de inicio de sesión del proveedor de transporte. Se ha soltado la memoria del objeto. 
    
6. MAPI o la cola MAPI llama a **FreeLibrary** en la dll del proveedor. 
    
Para una solidez, los objetos de inicio de sesión y proveedor deben ser capaces de controlar por sí mismos las llamadas de **versión** finales sin tener que llamar primero a sus métodos **TransportLogoff** o **Shutdown** . Si se llama a **Release** en estos casos, los proveedores de transporte deben tratar las llamadas como si se hubiera llamado a **TransportLogoff** o **Shutdown** con un argumento cero seguido de **Release**.
  

