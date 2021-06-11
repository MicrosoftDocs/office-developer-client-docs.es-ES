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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404298"
---
# <a name="designing-a-message-service"></a>Diseñar un servicio de mensajería

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Antes de empezar a escribir código para admitir el servicio de mensajes, es importante crear un diseño. Resuelva los siguientes problemas en el proceso de diseño:
  
1. Determine cuántos proveedores de servicios deben incluirse en el servicio de mensajes. Incluya solo proveedores de servicios relacionados (es decir, proveedores que trabajen con el mismo sistema de mensajería) en el servicio. Los proveedores de servicios no relacionados no pertenecen al mismo servicio de mensajes. Use el perfil para integrar proveedores de servicios y servicios de mensajes no relacionados.
    
2. Determine qué tipo de proveedores de servicios se deben incluir en el servicio de mensajes. La mayoría de los servicios de desorden incluyen un proveedor de cada uno de los tipos comunes. Es decir, el servicio de mensajes típico tiene un proveedor de libreta de direcciones, un proveedor de almacén de mensajes y un proveedor de transporte.
    
3. Determine cuántas DLL deben contener el servicio de mensajes. El número de DLL que usa un servicio de mensajes depende de lo siguiente:
    
   - Grado de complejidad que usted como escritor del servicio de mensajes está dispuesto a controlar.
    
   - Tipo de proveedores de servicios en el servicio de mensajes.
    
   - Relación que el servicio de mensajes puede tener con otro servicio de mensajes.
    
   Dado que MAPI almacena solo un punto de entrada para cada tipo de proveedor, no incluya varios proveedores del mismo tipo en un único ARCHIVO DLL. Si tiene sentido incluir varios proveedores de un tipo, puede implementarlos en DLL independientes o hacer que compartan una función de punto de entrada. Otra opción es implementar servicios de mensajes relacionados o servicios de mensajes que puedan usar el mismo código de instalación y configuración y la misma función de punto de entrada DLL, en un dll.
    
   Si es posible, manténlo sencillo y usa una DLL que contenga la implementación de todos los proveedores de servicios en el servicio de mensajes y todo el código para instalar y configurar el servicio de mensajes. Si esto no es posible, puede implementar un DLL para el código de instalación y configuración y un solo ARCHIVO DLL para todos los proveedores de servicios o un DLL para cada proveedor.
    
4. Determine un nombre para la DLL o dll del servicio de mensajes. 
    
## <a name="see-also"></a>Vea también

- [Implementación del servicio de mensajes](message-service-implementation.md)

