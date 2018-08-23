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
ms.openlocfilehash: 6460cd3ef0495a5494e03b4c7034e067cf8793b7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576067"
---
# <a name="attfrom"></a>attFrom

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El atributo **attFrom** se codifica como una estructura **TRP** que codifica la dirección para mostrar, nombre y correo electrónico del remitente, seguido por el nombre para mostrar y la dirección del remitente, seguido de cualquier relleno es necesario. El formato de **attFrom** es como sigue: 
  
**attFrom**: relleno de _TRP estructura_ remitente-display-name _ dirección remitente _ 
    
El nombre para mostrar de remitente es una cadena terminada en null que se rellena con un carácter nulo adicional, si es necesario ponerse en contacto con un límite de 2 bytes. El relleno al final de la codificación de **attFrom** consta de todos los caracteres null según sea necesario ponerse en contacto con un límite de **sizeof(TRP)** . 
  
_TRP estructura:_ **trpidOneOff** cbgrtrp cch cb 
    
Para el elemento **attFrom** , el **TRP**-estructura es siempre un uso único de codificación, por lo que el trpid desactiva el **TRP**-campo de estructura es siempre **trpidOneOff**. El cbgrtrp, cch y cb elementos corresponden a los campos restantes de la estructura **TRP** . 
  
El campo cbgrtrp se calcula como la suma de **(sizeof(TRP) \*2)**, la longitud del terminada en null remitente--nombre para mostrar con su relleno y la longitud de la dirección de remitente terminada en null.
  
El campo cch se calcula como la longitud del nombre para mostrar de terminada en null con su relleno.
  
El campo cb se calcula como la longitud de la dirección de remitente terminada en null.
  
_dirección de remitente:_ **:** de tipo de dirección de direcciones **'\0'**
    
La dirección del remitente es una cadena que consta de cuatro partes, el tipo de dirección, un carácter literal de dos puntos (:), la propia dirección y un carácter nulo. Por ejemplo, la cadena `fax:1-909-555-1234\0` sería un valor legal de la dirección del remitente.
  

