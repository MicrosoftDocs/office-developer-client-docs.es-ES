---
title: Implementar una función de punto de entrada de proveedor de servicios
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 40bbe110c7453cf2360fc103710fbc3bcb7f1c67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572056"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>Implementar una función de punto de entrada de proveedor de servicios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cada proveedor de servicios de DLL tiene una entrada de función que llama MAPI para cargarlo de punto. Tenga en cuenta que esta función de punto de entrada no es el mismo que [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), la función de punto de entrada de DLL de Win32.
  
Según el tipo de su proveedor, la función de punto de entrada de proveedor se ajusta a un prototipo diferente. MAPI define los prototipos de función de punto de entrada diferente para los proveedores de servicios.
  
|**Provider**|**Prototipo de función de punto de entrada**|
|:-----|:-----|
|Proveedores de almacén de mensajes  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Proveedores de transporte  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Proveedores de la libreta de direcciones  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
Gran parte de la funcionalidad de estos prototipos es el mismo para todos los tipos de proveedor de servicio. 
  
Libreta de direcciones, almacén de mensajes y los proveedores de transporte realizan las dos tareas principales siguientes en sus funciones de punto de entrada:
  
1. Comprobar la versión de la interfaz de proveedor de servicios (SPI) para asegurarse de que MAPI está usando una versión que sea compatible con la versión que está usando el proveedor de servicios. Use el parámetro _lpulMAPIVer_ , que contiene la versión de MAPI SPI y el parámetro _lpulProviderVer_ , que contiene la versión SPI, para realizar la comprobación. Estos parámetros son números enteros sin signo de 32 bits consta de tres partes: 
    
  - Bits 24 a 31 representan la versión principal.
    
  - Bits 16 a 23 representan la versión secundaria.
    
  - Bits 0 a 15 representan el identificador de la actualización. Aunque rara vez se cambia el número de versión principal, el número de versión secundaria cambios cada vez que se libera MAPI y ha cambiado el SPI. El identificador de actualización es el interno de Microsoft versión; de compilación se utiliza para realizar un seguimiento de los cambios durante el proceso de desarrollo. MAPI define la constante CURRENT_SPI_VERSION, que se documentaron en el archivo de encabezado Mapispi.h, para indicar la versión SPI presente. Producirá un error en la comprobación con el error MAPI_E_VERSION si está usando una versión de SPI que es más reciente que la versión que está utilizando MAPI.
    
2. Cree una instancia de un objeto de proveedor. Debido a que su proveedor puede ser iniciado e inicializado varias veces, debe crear una nueva instancia cada vez que esto ocurre. Los proveedores se inician varias veces cuando aparecen en varios perfiles que están en uso simultáneamente por uno o más clientes o cuando aparecen varias veces en un único perfil. Al igual que el prototipo de función de punto de entrada difiere según el tipo de su proveedor, también lo hace el tipo de objeto de proveedor. 
    
    Si está escribiendo un proveedor de la libreta de direcciones, implementar [IABProvider: IUnknown](iabprovideriunknown.md). Si está escribiendo un proveedor de almacén de mensajes, implementar [IMSProvider: IUnknown](imsprovideriunknown.md). Para obtener más información, vea [Cargar los proveedores de almacén de mensajes](loading-message-store-providers.md).
    
    Si está escribiendo un proveedor de transporte, implementar [IXPProvider: IUnknown](ixpprovideriunknown.md). Para obtener más información, vea [inicializar el proveedor de transporte](initializing-the-transport-provider.md).
    
## <a name="see-also"></a>Recursos adicionales



[Iniciar un proveedor de servicios](starting-a-service-provider.md)

