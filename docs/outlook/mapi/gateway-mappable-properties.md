---
title: Propiedades asignables de puerta de enlace
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321003"
---
# <a name="gateway-mappable-properties"></a>Propiedades asignables de puerta de enlace

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las propiedades asignables a la puerta de enlace son propiedades que pueden requerir traducción cuando se envían de un dominio de mensajería a otro. Las propiedades asignables a la puerta de enlace de MAPI permiten que los mensajes incluyan información que requiere una puerta de enlace para asegurarse de que el sistema de mensajería de destino la usa correctamente. Aunque no es necesario que los programadores de puertas de enlace proporcionen esta capacidad de traducción, deben considerar las propiedades asignables a la puerta de enlace como una oportunidad para mejorar el control del contenido de los mensajes.
  
MAPI especifica cinco tipos de propiedades asignables a la puerta de enlace:
  
- Nombre completo (DN)
    
- Nombre para mostrar
    
- Tipo de correo electrónico
    
- Identificador de entrada
    
- Clave de búsqueda
    
Este es el conjunto de propiedades de dirección asociadas con destinatarios, remitentes, destinatarios de informes y destinatarios y remitentes delegados. Para ayudar a su cliente a definir estas propiedades para que una puerta de enlace las controle de forma especial, MAPI especifica una Convención de nomenclatura usando propiedades y conjuntos de propiedades con nombre. Existen cinco conjuntos de propiedades para contener propiedades con nombre, las propiedades de direccionamiento que requieren asignación. Hay un conjunto de propiedades para cada tipo de propiedad asignable. Los conjuntos de propiedades que almacenarán estas propiedades de direccionamiento con nombre son los siguientes.
  
|**Conjunto de propiedades**|**Descripción**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Contiene las propiedades de cadena usadas como nombres para mostrar.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Contiene las propiedades de cadena usadas como direcciones de correo electrónico.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Contiene las propiedades de cadena usadas como tipos de dirección de correo electrónico.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Contiene propiedades binarias usadas como identificadores de entrada a largo plazo.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Contiene propiedades binarias usadas como claves de búsqueda.  <br/> |
   

