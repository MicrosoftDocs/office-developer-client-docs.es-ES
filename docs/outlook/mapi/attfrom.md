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
  
El **atributo attFrom** se codifica como una estructura **TRP** que codifica el nombre para mostrar y la dirección de correo electrónico del remitente, seguido del nombre para mostrar y la dirección del remitente, seguido de cualquier relleno necesario. El formato de **attFrom** es el siguiente: 
  
**attFrom**: _TRP-structure_ sender-display-name _ sender-address _ padding 
    
El sender-display-name es una cadena terminada en null que se agrega con un carácter nulo adicional, si es necesario, para alcanzar un límite de 2 bytes. El relleno al final de la codificación **attFrom** consta de tantos caracteres nulos como sea necesario para alcanzar un **límite sizeof(TRP).** 
  
_Estructura TRP:_ **trpidOneOff** cbgrtrp cch cb 
    
Para el **elemento attFrom,** **TRP**-structure siempre es una codificación única, por lo que el trpid del campo **TRP**-structure siempre **es trpidOneOff**. Los elementos cbgrtrp, cch y cb corresponden a los campos restantes de la **estructura TRP.** 
  
El campo cbgrtrp se calcula como la suma de **(sizeof(TRP) \* 2),** la longitud del nombre para mostrar del remitente terminado en null con su relleno y la longitud de la dirección del remitente terminada en null.
  
El campo cch se calcula como la longitud del nombre para mostrar terminado en null con su relleno.
  
El campo cb se calcula como la longitud de la dirección del remitente terminada en null.
  
_sender-address:_ address-type **:** address **'\0'**
    
La dirección del remitente es una cadena compuesta por cuatro partes, el tipo de dirección, dos puntos literales (:), la dirección en sí y un carácter nulo que termina. Por ejemplo, la cadena `fax:1-909-555-1234\0` sería un valor de dirección de remitente legal.
  

