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
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430360"
---
# <a name="mapi-transport-provider-objects"></a>Objetos de proveedor de transporte MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Además del proveedor estándar y los objetos de inicio de sesión implementados por todos los proveedores de servicios, los proveedores de transporte deben implementar un objeto de estado. Para los demás tipos de proveedor de servicios, la implementación de un objeto status es opcional. Sin embargo, MAPI lo requiere para los proveedores de transporte. Los proveedores de transporte que admiten la descarga de encabezados de mensaje desde un servidor remoto también implementan una carpeta y una tabla. 
  
En la siguiente ilustración se muestra cada uno de los objetos que los proveedores de transporte pueden implementar con sus interfaces correspondientes. La ilustración también indica si MAPI o un cliente es el usuario del objeto.
  
![Objetos que los proveedores de transporte implementan]Objetos que los proveedores de transporte(media/amapi_66.gif "implementan")
  
## <a name="see-also"></a>Vea también

- [Objetos del proveedor de servicios MAPI](mapi-service-provider-objects.md)

