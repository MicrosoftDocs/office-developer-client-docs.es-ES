---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 865d929f3348710b7786f4182670f3304a3a9244
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578041"
---
# <a name="attowner"></a>attOwner

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El atributo **attOwner** se codifica como cadenas contadas distribuyen to-end. El formato de **attOwner** es como sigue: 
  
 **attOwner**: 
  
> longitud del nombre para mostrar de nombre para mostrar dirección longitud _dirección de correo electrónico_
    
 _dirección de correo electrónico_
  
> dirección de tipo **:** 
    
A diferencia de otra longitud valores, la longitud del nombre para mostrar y la longitud de dirección son valores de 16 bits sin signo en lugar de enteros largos sin signo. Aún incluyen terminar caracteres null, sin embargo. Las cadenas de tipo y la dirección en la entrada de _dirección de correo electrónico_ están separadas por un carácter de dos puntos (:) literal, como "smtp:joe@nowhere.com". Sólo la cadena de dirección combinada del tipo **:** está terminada en null.
  
La asignación de las propiedades MAPI para el atributo **attOwner** depende de la clase de mensaje del mensaje que se va a codificar. 
  

