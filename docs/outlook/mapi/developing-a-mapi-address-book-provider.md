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
  
Un proveedor de libreta de direcciones proporciona información de destinatarios a las aplicaciones cliente, al almacén de mensajes y a los proveedores de transporte y a MAPI. La información del destinatario se organiza jerárquicamente en los compartimentos de almacenamiento conocidos como contenedores. Cada libreta de direcciones del perfil contribuye con uno o más contenedores de nivel superior o primario a la libreta de direcciones MAPI, una vista integrada de la información de destinatarios de todos los proveedores de libretas de direcciones de una sesión. Es a través de la libreta de direcciones MAPI que los clientes y otros proveedores de servicios obtienen acceso a los datos de un proveedor de libreta de direcciones.
  
MAPI compila la libreta de direcciones integrada mediante:
  
1. Recuperación de los contenedores de nivel superior de cada proveedor de libreta de direcciones.
    
2. Recuperación de la tabla de jerarquía de cada contenedor. 
    
3. Copiar cada tabla de jerarquía en una tabla de jerarquía integrada. Es la tabla de jerarquía integrada que se expone al cliente. 
    
MAPI impone pocos requisitos a los escritores de proveedores de libreta de direcciones. El rango de características posibles que puede implementar como escritor de libreta de direcciones es variado y flexible. Por ejemplo, su proveedor podría limitarse a proporcionar una vista de solo lectura de un tipo determinado de información de destinatarios o implementar un conjunto completo de características, lo que tal vez permita a los clientes o proveedores realizar adiciones o modificaciones en los datos del destinatario e imponer criterios de búsqueda para definir vistas personalizadas. 
  
Los datos del proveedor pueden residir localmente en un archivo o base de datos o en un servidor remoto. Algunos proveedores de libreta de direcciones están diseñados para trabajar con un sistema de mensajería determinado, estrechamente unido a un proveedor de transporte, mientras que otros pueden operar con cualquier sistema de mensajería.
  
MAPI define un tipo especial de proveedor de libreta de direcciones denominado libreta de direcciones personal, o PAB, que implementa un único contenedor modificable y puede contener información de destinatarios copiada de otros contenedores, así como información creada directamente. Aunque cualquier proveedor de libreta de direcciones puede implementar un PAB y varios PAB se pueden agregar a un perfil, solo uno de estos proveedores puede ser designado para funcionar como PAB durante cualquier sesión. 
  

