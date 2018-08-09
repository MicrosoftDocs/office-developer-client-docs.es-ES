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
ms.openlocfilehash: 03f53dbfbe57db76ee8ceefda3f6938301f70da8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816662"
---
# <a name="developing-a-mapi-address-book-provider"></a>Desarrollar un proveedor de libreta de direcciones MAPI

  
  
**Hace referencia a**: Outlook 
  
Un proveedor de la libreta de direcciones proporciona información de destinatarios a las aplicaciones cliente, al almacén de mensajes y de los proveedores, de transporte y a MAPI. Información de destinatarios se organiza jerárquicamente en compartimentos de almacenamiento conocidos como contenedores. Cada libreta de direcciones en el perfil de contribuye a uno o más nivel superior, o primario, los contenedores de la libreta de direcciones MAPI, una vista integrada de información de todas las direcciones de los destinatarios book proveedores en una sesión. Es a través de la libreta de direcciones MAPI que los clientes y otros proveedores de servicios de tener acceso a los datos de un proveedor de la libreta de direcciones.
  
MAPI basa la libreta de direcciones integrada por:
  
1. Recuperación de los contenedores de nivel superior de cada proveedor de la libreta de direcciones.
    
2. Recuperación de tabla de jerarquía de cada contenedor. 
    
3. Copiar cada tabla de jerarquía en una tabla de jerarquías integrada. Es la tabla de jerarquía integrada que se expone al cliente. 
    
MAPI impone algunos requisitos en los escritores de proveedor de la libreta de direcciones. El intervalo de posibles características se puede implementar como un sistema de escritura de la libreta de direcciones es variado y flexible. Por ejemplo, podría estar limitada a proporcionar una vista de solo lectura de un tipo determinado de información del destinatario o implementar un conjunto completo de características, quizás lo que permite los clientes o proveedores para realizar adiciones o modificaciones realizadas en los datos de destinatario y para imponer su proveedor de criterios de búsqueda para definir vistas personalizadas. 
  
Los datos de su proveedor pueden residir localmente en un archivo o una base de datos o en un servidor remoto. Algunos proveedores de libreta de direcciones están diseñados para trabajar con un sistema de mensajería determinado, estrechamente con un proveedor de transporte, mientras que otros usuarios pueden funcionar con cualquier sistema de mensajería.
  
MAPI define un tipo especial de proveedor de libreta de direcciones que llama a una libreta de direcciones personales o PAB, que implementa un único contenedor modificable y puede contener información de destinatarios copió desde otros contenedores, así como información creada directamente. Aunque cualquier proveedor de la libreta de direcciones puede implementar una PAB y varios PAB puede agregarse a un perfil, se puede designar sólo uno de estos proveedores para funcionar como el archivo PAB durante una sesión de prueba. 
  

