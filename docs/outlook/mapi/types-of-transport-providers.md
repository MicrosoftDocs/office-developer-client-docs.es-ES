---
title: Tipos de proveedores de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315382"
---
# <a name="types-of-transport-providers"></a>Tipos de proveedores de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todos los proveedores de transporte admiten una amplia variedad de características estándar, como:
  
- Proporciona una seguridad adecuada para el sistema de mensajería subyacente.
    
- Enviar y recibir mensajes del sistema de mensajería subyacente.
    
- Exposición de los tipos de dirección que admiten los proveedores de transporte para que la cola MAPI y las aplicaciones cliente puedan usarlos correctamente.
    
- Aceptar la entrega para destinatarios específicos.
    
Además, MAPI admite dos tipos de proveedores especializados para sistemas de mensajería específicos.
  
|**Tipo de transporte**|**Funcionalidad agregada**|
|:-----|:-----|
|Transporte remoto  <br/> |Habilita la interoperabilidad con los clientes conectados de forma remota.  <br/> |
|Transporte TNEF  <br/> |Permite que las propiedades MAPI se conserven en sistemas de mensajería que no las admiten.  <br/> |
   
Los transportes TNEF se usan para traducir mensajes entre sistemas de mensajería que admiten distintos conjuntos de propiedades MAPI. Los transportes TNEF usan la interfaz MAPI [ITnef: IUnknown](itnefiunknown.md) para convertir las propiedades que el sistema de destino no puede representar directamente en una secuencia de datos binarios que se puede adjuntar al mensaje. Más adelante, otro transporte TNEF puede usar **ITnef** para descodificar el flujo de datos y hacer que las propiedades MAPI originales estén disponibles para las aplicaciones cliente. Además, se requiere compatibilidad con TNEF si el transporte tiene que admitir clases de mensaje personalizadas. Para obtener información acerca de la implementación de transportes TNEF, consulte [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).
  
Si su proveedor de transporte no es uno de estos tipos, tendrá que implementarlo con las funciones MAPI básicas y las funciones de red disponibles en la plataforma de destino.
  

