---
title: Objetos de proveedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2d7311857ff54ef253fd00634671f4a510443f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818230"
---
# <a name="mapi-transport-provider-objects"></a>Objetos de proveedor de transporte MAPI
  
**Hace referencia a**: Outlook 
  
Además de los objetos de inicio de sesión implementados por todos los proveedores de servicio y proveedor estándar, los proveedores de transporte necesarios para implementar un objeto de estado. Para los demás tipos de proveedor servicio, la implementación de un objeto de estado es opcional. Sin embargo, MAPI requiere para los proveedores de transporte. Los proveedores de transporte que admiten la descarga de encabezados de los mensajes desde un servidor remoto también implementan una carpeta y una tabla. 
  
En la siguiente ilustración se muestra cada uno de los objetos que los proveedores de transporte se pueden implementar con sus interfaces correspondientes. En la ilustración también indica si MAPI o un cliente es usuario del objeto.
  
![Objetos que implementan los proveedores de transporte] (media/amapi_66.gif "Objetos que implementan los proveedores de transporte")
  
## <a name="see-also"></a>Vea también

- [Objetos de proveedor de servicio MAPI](mapi-service-provider-objects.md)

