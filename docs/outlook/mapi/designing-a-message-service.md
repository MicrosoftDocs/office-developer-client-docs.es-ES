---
title: Diseñar un servicio de mensajería
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 19a8a939685c440901f3f57d72baf673a579e590
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316726"
---
# <a name="designing-a-message-service"></a>Diseñar un servicio de mensajería

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Antes de empezar a escribir código para admitir el servicio de mensajes, es importante crear un diseño. Resuelva los problemas siguientes en el proceso de diseño:
  
1. Determinar cuántos proveedores de servicios deben incluirse en el servicio de mensajes. Incluya solo los proveedores de servicios relacionados (es decir, proveedores que trabajen con el mismo sistema de mensajería) en su servicio. Los proveedores de servicios no relacionados no pertenecen al mismo servicio de mensajes. Use el perfil para integrar proveedores de servicios no relacionados y servicios de mensajes.
    
2. DeTermine qué tipo de proveedores de servicios debe incluirse en el servicio de mensajes. La mayoría de los servicios de messge incluyen un proveedor de cada uno de los tipos comunes. Es decir, el servicio de mensajes típico tiene un proveedor de libretas de direcciones, un proveedor de almacenamiento de mensajes y un proveedor de transporte.
    
3. Determinar el número de dll que deben contener el servicio de mensajes. La cantidad de dll que usa un servicio de mensajes depende de lo siguiente:
    
   - El grado de complejidad que usted tiene como escritor del servicio de mensajes que desea controlar.
    
   - El tipo de proveedores de servicios en el servicio de mensajes.
    
   - La relación que el servicio de mensajes puede tener con otro servicio de mensajes.
    
   Como MAPI almacena solo un punto de entrada para cada tipo de proveedor, no incluya varios proveedores del mismo tipo en una única DLL. Si tiene sentido incluir varios proveedores de un tipo, puede implementarlos en dll distintas o hacer que compartan una función de punto de entrada. Otra opción consiste en implementar servicios de mensajes relacionados, o servicios de mensajes que puedan usar el mismo código de instalación y configuración y la misma función de punto de entrada de DLL, en un archivo DLL.
    
   Si es posible, Manténgase sencillo y use una DLL que contenga la implementación de todos los proveedores de servicios en el servicio de mensajes y todo el código para instalar y configurar el servicio de mensajes. Si esto no es posible, puede implementar una DLL para el código de instalación y configuración y una única DLL para todos los proveedores de servicios o una DLL para cada proveedor.
    
4. Determinar un nombre para la DLL o DLL de servicio de mensajes. 
    
## <a name="see-also"></a>Vea también

- [Implementación del servicio de mensajes](message-service-implementation.md)

