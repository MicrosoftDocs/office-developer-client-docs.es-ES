---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b292e65ddabcbe052832687a3dcf01658de5e379
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567478"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El atributo **attSentFor** se codifica como cadenas contadas distribuyen to-end. El formato de **attSentFor** es como sigue: 
  
 **attSentFor**: 
  
> longitud del nombre para mostrar de nombre para mostrar dirección longitud _dirección de correo electrónico_
    
 _dirección de correo electrónico_
  
> dirección de tipo **:** 
    
A diferencia de otra longitud valores, la longitud del nombre para mostrar y la longitud de dirección son valores de 16 bits sin signo en lugar de enteros largos sin signo. Aún incluyen terminar caracteres null, sin embargo. Las cadenas de tipo y la dirección en la entrada de _dirección de correo electrónico_ están separadas por un carácter de dos puntos (:) literal, como "smtp:joe@nowhere.com". Sólo la cadena de dirección combinada del tipo **:** está terminada en null.
  

