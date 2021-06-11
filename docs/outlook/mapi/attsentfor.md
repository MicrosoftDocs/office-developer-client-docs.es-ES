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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408841"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El **atributo attSentFor** se codifica como cadenas contadas establecidas de un extremo a otro. El formato de **attSentFor** es el siguiente: 
  
 **attSentFor**: 
  
> display-name-length display-name address-length  _email-address_
    
 _email-address_
  
> tipo **:** address 
    
A diferencia de otros valores de longitud, los valores para mostrar-name-length y address-length son valores de 16 bits sin signo en lugar de enteros largos sin signo. Sin embargo, aún incluyen los caracteres nulos de terminación. Las cadenas de tipo y dirección de la entrada  _de dirección de_ correo electrónico están separadas por dos puntos literales (:) carácter, como "smtp:joe@nowhere.com". Solo el tipo combinado **:** la cadena de dirección termina en null.
  

