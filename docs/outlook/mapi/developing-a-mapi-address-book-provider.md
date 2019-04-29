---
title: Desarrollar un proveedor de libreta de direcciones MAPI
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
# <a name="developing-a-mapi-address-book-provider"></a>Desarrollar un proveedor de libreta de direcciones MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de libreta de direcciones proporciona información de destinatarios a las aplicaciones cliente, a los proveedores de almacenamiento y transporte de mensajes y a MAPI. La información de los destinatarios se organiza jerárquicamente en compartimientos de almacenamiento conocidos como contenedores. Todas las libretas de direcciones del perfil aportan uno o varios contenedores de nivel superior, o primarios, a la libreta de direcciones MAPI, una vista integrada de la información de destinatarios de todos los proveedores de la libreta de direcciones en una sesión. A través de la libreta de direcciones MAPI, los clientes y otros proveedores de servicios obtienen acceso a los datos de un proveedor de la libreta de direcciones.
  
MAPI crea la libreta de direcciones integrada:
  
1. Recuperar los contenedores de nivel superior de cada proveedor de la libreta de direcciones.
    
2. Recuperar la tabla de jerarquías de cada contenedor. 
    
3. Copiando cada tabla de jerarquía en una tabla de jerarquía integrada. Se trata de la tabla de jerarquías integrada que se expone al cliente. 
    
MAPI impone pocos requisitos en los escritores del proveedor de la libreta de direcciones. El intervalo de características posibles que puede implementar como un escritor de la libreta de direcciones es muy flexible y variado. Por ejemplo, el proveedor puede limitarse a proporcionar una vista de solo lectura de un tipo concreto de información de destinatarios o implementar un conjunto completo de características, lo que permite a los clientes o a los proveedores realizar adiciones o modificaciones a los datos del destinatario y imponer Criterios de búsqueda para definir vistas personalizadas. 
  
Los datos de su proveedor pueden residir localmente en un archivo o base de datos o en un servidor remoto. Algunos proveedores de libretas de direcciones están diseñados para funcionar con un sistema de mensajería determinado, estrechamente acoplados con un proveedor de transporte, mientras que otros pueden operar con cualquier sistema de mensajería.
  
MAPI define un tipo especial de proveedor de libreta de direcciones denominado libreta personal de direcciones, o PAB, que implementa un solo contenedor modificable y puede almacenar la información de destinatarios copiada de otros contenedores, así como la información que se crea directamente. Aunque cualquier proveedor de libreta de direcciones puede implementar una PAB y varios PAB pueden agregarse a un perfil, solo se puede designar a uno de estos proveedores para que opere como PAB durante una sesión. 
  

