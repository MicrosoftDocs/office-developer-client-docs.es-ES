---
title: Diseño de un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 04aa4348560396c8237811252fd96a2b461cd791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816653"
---
# <a name="designing-a-message-service"></a>Diseño de un servicio de mensajes

**Se aplica a**: Outlook 
  
Antes de comenzar a escribir código para admitir el servicio de mensajes, es importante crear un diseño. Resolver los problemas siguientes en el proceso de diseño:
  
1. Determinar cuántos proveedores de servicios deben incluirse en el servicio de mensajes. Incluir sólo los proveedores de servicios relacionados (es decir, los proveedores que funcionan con el mismo sistema de mensajería) en su servicio. Proveedores de servicios no relacionados no pertenecen en el mismo servicio de mensajes. Utilice el perfil de la integración de proveedores de servicios no relacionados y servicios de mensajes.
    
2. Determinar qué tipo de proveedores de servicios debe incluirse en el servicio de mensajes. La mayoría de los servicios de mensaje incluye un proveedor de cada uno de los tipos comunes. Es decir, el servicio de mensajes típico tiene proveedor de libretas de direcciones, proveedor de almacenamiento de un mensaje y proveedor de uno transporte.
    
3. Determinar cuántos archivos DLL debe contener el servicio de mensajes. El número de archivos DLL que usa un servicio de mensajes depende de lo siguiente:
    
   - El grado de complejidad que usted, como el escritor del servicio de mensajes está dispuestos a controlar.
    
   - El tipo de proveedores de servicios en el servicio de mensajes.
    
   - La relación que podría tener el servicio de mensajes con otro servicio de mensajes.
    
   Debido a que MAPI almacena sólo un punto de entrada para cada tipo de proveedor, no incluya varios proveedores del mismo tipo en un solo archivo DLL. Si tiene sentido para incluir varios proveedores de un tipo, puede implementarlos en archivos DLL independientes o hacer que comparten una función de punto de entrada. Otra opción consiste en implementar servicios de mensajes relacionados o servicios de mensajes que se pueden utilizar la misma instalación y código de configuración y el misma archivo DLL punto de entrada (función), en un archivo DLL.
    
   Si es posible, mantener simple y usar una DLL que contiene la implementación de todos los proveedores de servicio en el servicio de mensajes y todo el código para instalar y configurar el servicio de mensajes. Si esto no es posible, se puede implementar una DLL para el código de instalación y configuración y ya sea un solo archivo DLL para todos los proveedores de servicios o un archivo DLL para cada proveedor.
    
4. Determinar un nombre para el servicio de mensajes DLL o archivos DLL. 
    
## <a name="see-also"></a>Ver también

- [Implementación del servicio de mensajes](message-service-implementation.md)

