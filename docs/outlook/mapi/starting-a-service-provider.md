---
title: Inicio de un proveedor de servicios
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439558"
---
# <a name="starting-a-service-provider"></a>Inicio de un proveedor de servicios

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En algún momento después de que un cliente inicie una sesión con MAPI, se iniciará el proveedor de servicios. Los proveedores de transporte se inician cuando un cliente realiza una solicitud para sus servicios. Los proveedores de libreta de direcciones y almacén de mensajes se inician durante el proceso de inicio de sesión del cliente.
  
Un cliente llama a [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para cargar cada uno de los proveedores de libretas de direcciones incluidos en el perfil y [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) para cargar un proveedor de almacén de mensajes específico. Los proveedores de libretas de direcciones que forman parte de un servicio de mensajes se inician antes que cualquier otro proveedor del servicio. 
  
MAPI inicia cada proveedor de servicios en el perfil activo haciendo lo siguiente:
  
- Buscar el nombre de su DLL en el perfil. Debe registrar el nombre de la DLL del proveedor en el archivo de configuración Mapisvc.inf para asegurarse de que aparece en el perfil. Cuando el proveedor de servicios se agrega a un perfil, ya sea individualmente o como parte de un servicio de mensajes, todas las secciones [Proveedor de **servicios]** de Mapisvc.inf que se aplican al proveedor se copian en el perfil. Para obtener más información acerca de la estructura de Mapisvc.inf, vea formato [de archivo de MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
- Llamar a la función **loadLibrary** de la API de Windows para cargar la DLL. Dado que MAPI llama a **LoadLibrary** cada vez que usa una DLL del proveedor de servicios (independientemente de si ya se ha cargado) o solo la primera vez, el proveedor de servicios no debe hacer suposiciones sobre el número de veces que se cargará. Por cada llamada a **LoadLibrary**, MAPI realiza una llamada a la función de la API de Windows **FreeLibrary** cuando ya no se necesita una DLL del proveedor de servicios. 
    
- Llamar a la función de punto de entrada para el proveedor. MAPI llama a la función de punto de entrada del proveedor para iniciar el proceso de inicio de sesión. Las funciones de punto de entrada garantizan el uso de una versión de la interfaz del proveedor de servicios (SPI) compatible con la versión que usa MAPI. Estas funciones también devuelven punteros a objetos de proveedor recién creados. Para obtener más información acerca de cómo crear una función de punto de entrada para su proveedor, vea Implementar una función de punto de entrada [del proveedor de servicios.](implementing-a-service-provider-entry-point-function.md)
    
## <a name="see-also"></a>Consulte también



[Proveedores de servicios MAPI](mapi-service-providers.md)

