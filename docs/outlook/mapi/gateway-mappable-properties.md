---
title: Pueda asignables propiedades de puerta de enlace
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b637f4921165d70ddeda914b4299c35aabe8218f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816898"
---
# <a name="gateway-mappable-properties"></a>Pueda asignables propiedades de puerta de enlace

**Hace referencia a**: Outlook 
  
Propiedades pueda asignar la puerta de enlace son propiedades que es posible que requieren conversión cuando se envían desde un dominio de mensajería a otro. Propiedades pueda asignar la puerta de enlace de MAPI permiten los mensajes incluir información que requiere una puerta de enlace para asegurarse de que el sistema de mensajería de destino lo usa correctamente. Aunque los programadores de puerta de enlace no son necesarias para proporcionar esta capacidad de traducción, deben tener en cuenta las propiedades pueda asignar la puerta de enlace como una oportunidad para mejorar el control de contenido de mensaje.
  
MAPI especifica cinco tipos de propiedades pueda asignar la puerta de enlace:
  
- Nombre para mostrar
    
- Dirección de correo electrónico
    
- Tipo de correo electrónico
    
- Identificador de entrada
    
- Clave de búsqueda
    
Éste es el conjunto de hacer frente a las propiedades que se asocian con los destinatarios, remitentes, destinatarios de los informes y delegados remitentes y destinatarios. Para ayudar a su cliente a definir estas propiedades para que una puerta de enlace los controle especialmente, MAPI especifica una convención de nomenclatura con conjuntos de propiedades y las propiedades con nombre. Existen cinco conjuntos de propiedades para contener propiedades con nombre, las propiedades de direccionamiento que requieren la asignación. Hay una propiedad establecido para cada tipo de propiedad pueda asignar. Los conjuntos de propiedades que contendrá estas propiedades direccionamiento con nombre son los siguientes.
  
|**Conjunto de propiedades**|**Descripción**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Contiene propiedades de cadena que se usan como nombres para mostrar.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Contiene propiedades de cadena que se usan como direcciones de correo electrónico.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Contiene propiedades de cadena que se usan como tipos de direcciones de correo electrónico.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Contiene propiedades binario que se usan como identificadores de entrada a largo plazo.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Contiene propiedades binario que se usan como claves de búsqueda.  <br/> |
   

