---
title: Desarrollo de un proveedor de libreta de direcciones MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409373"
---
# <a name="developing-a-mapi-address-book-provider"></a>Desarrollo de un proveedor de libreta de direcciones MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de libreta de direcciones proporciona información de destinatarios a las aplicaciones cliente, a los proveedores de almacenamiento y transporte de mensajes y a MAPI. La información del destinatario se organiza jerárquicamente en compartimentos de almacenamiento conocidos como contenedores. Cada libreta de direcciones del perfil contribuye a uno o más contenedores de nivel superior o primario a la libreta de direcciones MAPI, una vista integrada de la información del destinatario de todos los proveedores de libretas de direcciones en una sesión. A través de la libreta de direcciones MAPI, los clientes y otros proveedores de servicios obtienen acceso a los datos de un proveedor de libreta de direcciones.
  
MAPI crea la libreta de direcciones integrada mediante:
  
1. Recuperación de los contenedores de nivel superior de cada proveedor de libreta de direcciones.
    
2. Recuperación de la tabla de jerarquía de cada contenedor. 
    
3. Copiar cada tabla de jerarquía en una tabla de jerarquía integrada. Es la tabla de jerarquía integrada que se expone al cliente. 
    
MAPI impone pocos requisitos a los escritores de proveedores de libretas de direcciones. La gama de posibles características que puede implementar como escritor de libretas de direcciones es variada y flexible. Por ejemplo, el proveedor podría limitarse a proporcionar una vista de solo lectura de un tipo determinado de información de destinatario o a implementar un conjunto completo de características, lo que podría permitir a los clientes o proveedores realizar adiciones o modificaciones a los datos del destinatario e imponer criterios de búsqueda para definir vistas personalizadas. 
  
Los datos del proveedor pueden residir localmente en un archivo o base de datos o en un servidor remoto. Algunos proveedores de libretas de direcciones están diseñados para trabajar con un sistema de mensajería determinado, estrechamente unido a un proveedor de transporte, mientras que otros pueden funcionar con cualquier sistema de mensajería.
  
MAPI define un tipo especial de proveedor de libreta de direcciones denominado libreta de direcciones personal, o PAB, que implementa un único contenedor modificable y puede contener información de destinatarios copiada de otros contenedores, así como información creada directamente. Aunque cualquier proveedor de libreta de direcciones puede implementar un PAB y se pueden agregar varias PAB a un perfil, solo se puede designar uno de estos proveedores para que funcione como pab durante cualquier sesión. 
  

