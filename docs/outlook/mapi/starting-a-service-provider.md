---
title: Iniciar un proveedor de servicios
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 99f47ee4fe990b0e77fcf868977b72d83bfdbac7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820759"
---
# <a name="starting-a-service-provider"></a>Iniciar un proveedor de servicios

 
  
**Se aplica a**: Outlook 
  
En algún momento después de que un cliente inicia una sesión con MAPI, su proveedor de servicios se iniciarán. Los proveedores de transporte se inician cuando un cliente realiza una solicitud para sus servicios. Proveedores de almacén de libreta de direcciones y el mensaje de dirección se inician durante el proceso de inicio de sesión del cliente.
  
Un cliente llama a [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para cada uno de los proveedores de libreta de direcciones incluidos en el perfil y [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) cargar un proveedor de almacén de mensaje específico de carga. Los proveedores de la libreta de direcciones que forman parte de un servicio de mensajes se hayan iniciado antes de cualquiera de los otros proveedores en el servicio. 
  
MAPI inicia cada proveedor de servicios en el perfil activo haciendo lo siguiente:
  
- Localizar el nombre de su archivo DLL en el perfil. Son necesarios para registrar el nombre del proveedor de DLL en el archivo Mapisvc.inf de configuración para asegurarse de que aparece en el perfil. Cuando su proveedor de servicios se agrega a un perfil, ya sea individualmente o como parte de un servicio de mensajes, todas las secciones **[Servicio proveedor]** desde Mapisvc.inf que se aplican a su proveedor se copian en el perfil. Para obtener más información acerca de la estructura de Mapisvc.inf, vea [Formato de archivo de MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
- Llamar a la función **LoadLibrary** para cargar el archivo DLL de API de Windows. Debido a que las llamadas de MAPI **LoadLibrary** uno cada vez que usa un proveedor de servicios DLL (independientemente de si ya se ha cargado) o sólo la primera vez, su proveedor de servicios no debe hacer suposiciones sobre el número de veces que se va a cargar. Para todas las llamadas a **LoadLibrary**, MAPI realiza una llamada a la función **FreeLibrary** cuando un proveedor de servicios que ya no se necesita el archivo DLL de API de Windows. 
    
- Llamar a la función de punto de entrada para el proveedor. MAPI llama a la función de punto de entrada de su proveedor para iniciar el proceso de inicio de sesión. Funciones de punto de entrada Asegúrese de que está usando una versión de la interfaz de proveedor de servicios (SPI) que es compatible con la versión que se está usa de MAPI. Estas funciones también devuelven punteros a objetos de proveedor recién creado. Para obtener más información sobre la creación de una entrada de función de punto de su proveedor, vea [implementar una función de punto de servicio de proveedor de entrada](implementing-a-service-provider-entry-point-function.md).
    
## <a name="see-also"></a>Ver también



[Proveedores de servicios de MAPI](mapi-service-providers.md)

