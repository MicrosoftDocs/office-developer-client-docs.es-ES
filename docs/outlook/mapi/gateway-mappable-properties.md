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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430479"
---
# <a name="gateway-mappable-properties"></a>Propiedades asignables de puerta de enlace

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las propiedades asignables a la puerta de enlace son propiedades que pueden requerir traducción cuando se envían de un dominio de mensajería a otro. Las propiedades asignables a la puerta de enlace de MAPI permiten que los mensajes incluyan información que requiere una puerta de enlace para garantizar que el sistema de mensajería de destino la usa correctamente. Aunque no es necesario que los desarrolladores de puertas de enlace proporcionen esta funcionalidad de traducción, deben considerar las propiedades asignables a la puerta de enlace como una oportunidad para mejorar el control del contenido de los mensajes.
  
MAPI especifica cinco tipos de propiedades asignables a la puerta de enlace:
  
- Nombre completo (DN)
    
- Nombre para mostrar
    
- Tipo de correo electrónico
    
- Identificador de entrada
    
- Clave de búsqueda
    
Este es el conjunto de propiedades de direccionamiento asociadas a destinatarios, remitentes, destinatarios de informes y remitentes y destinatarios delegados. Para ayudar al cliente a definir estas propiedades para que una puerta de enlace las controle especialmente, MAPI especifica una convención de nomenclatura mediante propiedades con nombre y conjuntos de propiedades. Existen cinco conjuntos de propiedades para contener propiedades con nombre, las propiedades de direccionamiento que requieren asignación. Hay una propiedad establecida para cada tipo de propiedad asignable. Los conjuntos de propiedades que contendrán estas propiedades de direccionamiento con nombre son los siguientes.
  
|**Conjunto de propiedades**|**Descripción**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Contiene propiedades de cadena usadas como nombres para mostrar.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Contiene propiedades de cadena usadas como direcciones de correo electrónico.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Contiene propiedades de cadena usadas como tipos de direcciones de correo electrónico.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Contiene propiedades binarias usadas como identificadores de entrada a largo plazo.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Contiene propiedades binarias usadas como claves de búsqueda.  <br/> |
   

