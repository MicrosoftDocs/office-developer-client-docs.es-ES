---
title: Implementación de una función de punto de entrada del proveedor de servicios
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332994"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>Implementación de una función de punto de entrada del proveedor de servicios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cada DLL del proveedor de servicios tiene una función de punto de entrada a la que MAPI llama para cargarla. Tenga en cuenta que esta función de punto de entrada no es la misma que [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), la función de punto de entrada dll de Win32.
  
Según el tipo de proveedor, la función de punto de entrada del proveedor se ajusta a un prototipo diferente. MAPI define diferentes prototipos de función de punto de entrada para proveedores de servicios.
  
|**Provider**|**Prototipo de función de punto de entrada**|
|:-----|:-----|
|Proveedores de al almacenamiento de mensajes  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Proveedores de transporte  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Proveedores de libretas de direcciones  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
Gran parte de la funcionalidad de estos prototipos es la misma para todos los tipos de proveedor de servicios. 
  
Los proveedores de libreta de direcciones, almacén de mensajes y transporte realizan las dos tareas principales siguientes en sus funciones de punto de entrada:
  
1. Compruebe la versión de la interfaz del proveedor de servicios (SPI) para asegurarse de que MAPI está usando una versión compatible con la versión que está usando el proveedor de servicios. Use el  _parámetro lpulMAPIVer,_ que contiene la versión SPI de MAPI, y el parámetro  _lpulProviderVer,_ que contiene la versión SPI, para realizar la comprobación. Estos parámetros son enteros sin signo de 32 bits compuestos por tres partes: 
    
  - Los bits del 24 al 31 representan la versión principal.
    
  - Los bits 16 a 23 representan la versión secundaria.
    
  - Los bits del 0 al 15 representan el identificador de actualización. Aunque el número de versión principal rara vez cambia, el número de versión secundaria cambia siempre que mapi se libera y el SPI ha cambiado. El identificador de actualización es la versión de compilación interna de Microsoft; se usa para realizar un seguimiento de los cambios durante el proceso de desarrollo. MAPI define la CURRENT_SPI_VERSION, documentada en el archivo de encabezado Mapispi.h, para indicar la versión actual de SPI. No compruebe el error MAPI_E_VERSION si está usando una versión del SPI más reciente que la versión que usa MAPI.
    
2. Cree una instancia de un objeto de proveedor. Dado que el proveedor se puede iniciar e inicializar varias veces, debe crear una nueva instancia cada vez que esto ocurra. Los proveedores se inician varias veces cuando aparecen en varios perfiles que están en uso simultáneamente por uno o varios clientes, o cuando aparecen varias veces en un solo perfil. Al igual que el prototipo de función de punto de entrada difiere en función del tipo de proveedor, también lo hace el tipo de objeto de proveedor. 
    
    Si está escribiendo un proveedor de libreta de direcciones, implemente [IABProvider : IUnknown](iabprovideriunknown.md). Si está escribiendo un proveedor de almacenamiento de mensajes, implemente [IMSProvider : IUnknown](imsprovideriunknown.md). Para obtener más información, vea [Cargar proveedores de almacén de mensajes.](loading-message-store-providers.md)
    
    Si está escribiendo un proveedor de transporte, implemente [IXPProvider : IUnknown](ixpprovideriunknown.md). Para obtener más información, vea [Inicializar el proveedor de transporte.](initializing-the-transport-provider.md)
    
## <a name="see-also"></a>Consulte también



[Inicio de un proveedor de servicios](starting-a-service-provider.md)

