---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432418"
---
# <a name="attfrom"></a>attFrom

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El atributo **attFrom** se codifica como una estructura **TRP** que codifica el nombre para mostrar y la dirección de correo electrónico del remitente, seguido del nombre para mostrar y la dirección del remitente, seguido de cualquier relleno necesario. El formato para **attFrom** es el siguiente: 
  
**attFrom**: _TRP-Structure_ Sender-Display-Name _ Sender-Address _ padding 
    
Sender-Display-Name es una cadena terminada en null que se rellena con un carácter null adicional, si es necesario, para alcanzar un límite de 2 bytes. El relleno al final de la codificación **attFrom** consta de todos los caracteres nulos que se necesitan para alcanzar un límite **sizeof (TRP)** . 
  
_TRP-estructura:_ **trpidOneOff** cbgrtrp CCH CB 
    
Para el elemento **attFrom** , la estructura **TRP**es siempre una codificación de uso único, por lo que la trpid fuera del campo de la estructura **TRP**es siempre **trpidOneOff**. Los elementos cbgrtrp, CCH y CB corresponden a los demás campos de la estructura **TRP** . 
  
El campo cbgrtrp se calcula como la suma de **(sizeof (TRP \*) 2)**, la longitud del Sender-Display-Name con su relleno y la longitud de la dirección de remitente-terminada en NULL.
  
El campo CCH se calcula como la longitud del nombre para mostrar terminada en NULL con su relleno.
  
El campo CB se calcula como la longitud de la dirección de remitente-terminada en nulo.
  
_Sender-Address:_ Dirección-tipo **:** dirección **' \ 0 '**
    
La dirección del remitente es una cadena compuesta por cuatro partes, el tipo de dirección, un literal de dos puntos (:), la propia dirección y un carácter null de terminación. Por ejemplo, la cadena `fax:1-909-555-1234\0` sería un valor de remitente-dirección válido.
  

