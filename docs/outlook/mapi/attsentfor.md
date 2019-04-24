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
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318119"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El atributo **attSentFor** está codificado como cadenas contadas contenidas en un extremo a otro. El formato para **attSentFor** es el siguiente: 
  
 **attSentFor**: 
  
> Display-Name-length nombre-longitud de dirección dirección de _correo electrónico-dirección_
    
 _Dirección de correo electrónico_
  
> tipo **:** Address 
    
A diferencia de otros valores de longitud, Display-Name-length and Address-length son valores de 16 bits sin signo en lugar de enteros largos sin signo. Sin embargo, aún incluyen el final de los caracteres nulos. Las cadenas de tipo y dirección de la entrada de _dirección de correo electrónico_ están separadas por dos puntos literales (:) carácter, como "SMTP:Joe@nowhere.com". Solo el tipo combinado **:** la cadena de dirección termina en NULL.
  

