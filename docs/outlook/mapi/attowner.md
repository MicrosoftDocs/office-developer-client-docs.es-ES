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
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427657"
---
# <a name="attowner"></a>attOwner

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El **atributo attOwner** se codifica como cadenas contadas establecidas de un extremo a otro. El formato de **attOwner** es el siguiente: 
  
 **attOwner**: 
  
> display-name-length display-name address-length  _email-address_
    
 _email-address_
  
> tipo **:** address 
    
A diferencia de otros valores de longitud, los valores para mostrar-name-length y address-length son valores de 16 bits sin signo en lugar de enteros largos sin signo. Sin embargo, aún incluyen los caracteres nulos de terminación. Las cadenas de tipo y dirección de la entrada  _de dirección de_ correo electrónico están separadas por dos puntos literales (:) carácter, como "smtp:joe@nowhere.com". Solo el tipo combinado **:** la cadena de dirección termina en null.
  
La asignación de propiedades MAPI al **atributo attOwner** depende de la clase de mensaje del mensaje que se codifica. 
  

