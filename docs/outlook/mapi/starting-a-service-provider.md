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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341716"
---
# <a name="starting-a-service-provider"></a>Inicio de un proveedor de servicios

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En algún momento después de que un cliente inicia una sesión con MAPI, se iniciará el proveedor de servicios. Los proveedores de transporte se inician cuando un cliente realiza una solicitud de sus servicios. La libreta de direcciones y los proveedores de almacenamiento de mensajes se inician durante el proceso de inicio de sesión del cliente.
  
Un cliente llama a [IMAPISession:: OpenAddressBook](imapisession-openaddressbook.md) para cargar cada uno de los proveedores de libreta de direcciones incluidos en el perfil y [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) para cargar un proveedor de almacén de mensajes específico. Los proveedores de libreta de direcciones que forman parte de un servicio de mensajes se inician antes que los demás proveedores del servicio. 
  
MAPI inicia cada proveedor de servicios en el perfil activo de la siguiente manera:
  
- Buscar el nombre de su DLL en el perfil. Es necesario que registre el nombre de la DLL del proveedor en el archivo de configuración MAPISVC. inf para asegurarse de que aparece en el perfil. Cuando el proveedor de servicios se agrega a un perfil, ya sea de forma individual o como parte de un servicio de mensajes, todas las secciones **[proveedor de servicios]** de MAPISVC. inf que se aplican a su proveedor se copian en el perfil. Para obtener más información acerca de la estructura de MAPISVC. inf, consulte [formato de archivo de MAPISVC. inf](file-format-of-mapisvc-inf.md).
    
- Llamar a la función de la API de Windows **LoadLibrary** para cargar el archivo dll. Como MAPI llama a **LoadLibrary** cada vez que usa un archivo DLL del proveedor de servicios (independientemente de si ya se ha cargado) o sólo la primera vez, el proveedor de servicios no debe realizar suposiciones sobre el número de veces que se cargará. Por cada llamada a **LoadLibrary**, MAPI realiza una llamada a la función **FREELIBRARY** de la API de Windows cuando ya no se necesita un archivo DLL del proveedor de servicios. 
    
- Llamar a la función de punto de entrada para el proveedor. MAPI llama a la función de punto de entrada de su proveedor para iniciar el proceso de inicio de sesión. Las funciones de punto de entrada garantizan que se está usando una versión de la interfaz del proveedor de servicios (SPI) que es compatible con la versión que usa MAPI. Estas funciones también devuelven punteros a objetos de proveedor recién creados. Para obtener más información acerca de la creación de una función de punto de entrada para el proveedor, vea [implementar una función de punto de entrada de proveedor de servicios](implementing-a-service-provider-entry-point-function.md).
    
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

