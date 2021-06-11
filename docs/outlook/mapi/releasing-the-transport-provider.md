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

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando MAPI o la cola MAPI terminen de usar un objeto de inicio de sesión de transporte:
  
1. MAPI o la cola MAPI llama al método [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) del proveedor de transporte. 
    
2. El proveedor de transporte invalida el objeto status llamando al [método IMAPISupport::MakeInvalid.](imapisupport-makeinvalid.md) Si el proveedor de transporte invalida los objetos de mensaje que se envían o reciben en el momento de la llamada **TransportLogoff** depende de las marcas que se pasaron a **TransportLogoff**.
    
3. El proveedor de transporte llama al método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del objeto de soporte técnico para quitar la fila del proveedor de transporte de la tabla de estado y quitar de las tablas internas los identificadores únicos (UID) que se han establecido con el método [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md) Disminuye el número de objetos de inicio de sesión conocidos activos en este objeto de proveedor. Si el recuento alcanza cero, MAPI llama al [método IXPProvider::Shutdown](ixpprovider-shutdown.md) **y a Release** en el objeto de proveedor. Si este era el último objeto de proveedor conocido que usaba este ARCHIVO DLL en este proceso, MAPI llama a la **función FreeLibrary** en la DLL más adelante. Se libera la memoria del objeto de soporte técnico MAPI y devuelve el **método Release del objeto** de soporte técnico. 
    
4. El **método TransportLogoff** devuelve S_OK. 
    
5. MAPI o la cola MAPI llama **a Release** en el objeto de inicio de sesión del proveedor de transporte. Se libera la memoria del objeto. 
    
6. MAPI o la cola MAPI llama **a FreeLibrary** en el DLL del proveedor. 
    
Para mayor solidez, los objetos de inicio de sesión y proveedor deben poder controlar las llamadas finales **de** release por sí mismos sin llamar primero a sus **métodos TransportLogoff** o **Shutdown.** Si **se** llama a Release en estos casos, los proveedores de transporte deben tratar las llamadas como si se hubiera llamado a **TransportLogoff** o **Shutdown** con un argumento cero seguido de **Release**.
  

