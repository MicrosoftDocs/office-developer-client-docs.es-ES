---
title: Introducción al proveedor de servicios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: bc25158daa9579b5cd6cebe1eee878bf087762a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431431"
---
# <a name="mapi-service-provider-overview"></a>Introducción al proveedor de servicios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Entre el subsistema MAPI y los sistemas de mensajería se encuentran los distintos proveedores de servicios. Los proveedores de servicios son como controladores que conectan aplicaciones cliente MAPI a un sistema de mensajería subyacente. Hay tres tipos de proveedores: proveedores de almacén de mensajes, libreta de direcciones o proveedores de directorios y proveedores de transporte de mensajes. MAPI admite cada tipo de servicio de forma independiente, lo que permite a un proveedor ofrecer uno o más proveedores de servicios personalizados. Por ejemplo, es posible que un proveedor desee crear un proveedor de libreta de direcciones que use un directorio de libreta de teléfonos corporativo de empleados o crear un proveedor de almacén de mensajes que use una base de datos existente.
  
Los proveedores de servicios suelen estar escritos para sistemas de mensajería específicos por desarrolladores de software que tienen conocimientos especializados o experiencia con un sistema en particular. Por ejemplo, Microsoft Outlook 2013 y Microsoft Outlook 2010 Mobile Services un proveedor de libreta de direcciones para exponer una libreta de direcciones móvil en Outlook. 
  
MAPI presenta aplicaciones cliente con una vista unificada de la información del proveedor de transporte y libreta de direcciones. Este enfoque integrado impide que la aplicación cliente tenga que asignar datos al proveedor adecuado. También evita que el usuario tenga que negociar entre varios esquemas de direccionamiento de libreta de direcciones y proveedor de transporte. Sin embargo, la información del proveedor del almacén de mensajes no está unificada y los clientes que usan varios proveedores de almacén de mensajes son responsables de controlarlos individualmente.
  
Los proveedores de servicios trabajan con MAPI para crear y enviar mensajes de la siguiente manera: los mensajes se crean mediante un formulario adecuado para el tipo o clase específicos de mensaje. Muchos mensajes se realizan con el formulario de nota estándar que viene con el subsistema MAPI, ya sea por el usuario de una aplicación cliente o mediante programación sin interacción del usuario. El mensaje completado se dirige a uno o varios destinatarios: un usuario o grupo de usuarios designados para recibir el mensaje. Un destinatario puede o no tener una entrada en un directorio que uno de los proveedores de libreta de direcciones instalados posee. Los destinatarios que no están asociados con un proveedor de libreta de direcciones instalado se denominan destinatarios personalizados o direcciones únicas. Una dirección de uso único puede ser temporal y solo dura hasta que se envía el mensaje. 
  
Cuando la aplicación cliente envía el mensaje, el proveedor del almacén de mensajes comprueba que cada destinatario tiene una dirección única y válida y que el mensaje tiene toda la información necesaria para la transmisión. Si hay una pregunta sobre un destinatario (por ejemplo, cuando hay varios destinatarios con el mismo nombre), un proveedor de libreta de direcciones se encarga de resolver la ambigüedad. A continuación, el mensaje se coloca en la cola de salida. 
  
## <a name="see-also"></a>Vea también



[Características y arquitectura MAPI](mapi-features-and-architecture.md)

