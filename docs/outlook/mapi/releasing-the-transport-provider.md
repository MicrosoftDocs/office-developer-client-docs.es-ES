---
title: Publicar el proveedor de transporte
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: 'Última modificación: 07 de diciembre de 2015'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386225"
---
# <a name="releasing-the-transport-provider"></a>Publicar el proveedor de transporte

 
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Cuando MAPI o la cola MAPI termina de usar un objeto de inicio de sesión de transporte:
  
1. MAPI o la cola MAPI llama (método [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) ) del proveedor de transporte. 
    
2. El proveedor de transporte invalida el objeto de estado llamando al método [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) . Si el proveedor de transporte invalida los objetos de mensaje que se va a enviados o recibidos en el momento de la llamada **TransportLogoff** dependen de los indicadores que se han pasado a **TransportLogoff**.
    
3. El proveedor de transporte llama a [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) (método) del objeto de soporte técnico para quitar la fila del proveedor de transporte de la tabla de estado y quitar de las tablas internas cualquier identificadores únicos (UID) que se han establecido con el [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) (método). Se disminuye el recuento de objetos de inicio de sesión conocido activos en este objeto de proveedor. Si el recuento llega a cero, MAPI llama al método [IXPProvider::Shutdown](ixpprovider-shutdown.md) y la **versión** en el objeto de proveedor. Si éste era el último objeto de proveedor conocidos con este archivo DLL en este proceso, MAPI llama a la función **FreeLibrary** en el archivo DLL en un momento posterior. Se libera memoria para el objeto de soporte técnico MAPI y devuelve el objeto compatible con el método de **versión** . 
    
4. El método **TransportLogoff** devuelve S_OK. 
    
5. MAPI o la cola MAPI llama a **Release** en el objeto de inicio de sesión del proveedor de transporte. Se libera la memoria para el objeto. 
    
6. MAPI o la cola MAPI llama **FreeLibrary** en el archivo DLL del proveedor. 
    
Para solidez, los objetos de inicio de sesión y proveedor deben ser capaces de controlar las llamadas de **versión** finales en ellos mismos sin tener primero sus **TransportLogoff** o métodos que se **cierre** llama. Si se llama a **Release** en tales casos, los proveedores de transporte deben tratar las llamadas como si hubiera llamado **TransportLogoff** o **apagado** con un cero argumento seguido de **Release**.
  

