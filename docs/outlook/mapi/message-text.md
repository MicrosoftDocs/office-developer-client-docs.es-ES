---
title: Texto del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d1837f1-494f-481b-9e09-ab8249f1488c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fcbdec5adcb47ffac431a832cbb851ee4ebe16d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418550"
---
# <a name="message-text"></a>Texto del mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para los mensajes salientes en modo MIME, el tipo de contenido depende de si hay datos adjuntos y el aspecto del texto del mensaje. Si hay datos adjuntos, el tipo de contenido es de _varias partes/mixto;_ el texto del mensaje y cada adjunto se convierten en una parte independiente del contenido del mensaje, cada uno con su propio tipo de contenido. Si no hay datos adjuntos, el tipo de contenido del mensaje es _texto/sin formato_ y solo hay una parte. 
  
El texto del mensaje no se ajusta en línea a menos que alguna línea supere los 140 caracteres de longitud. Si lo hace, se ajusta el texto completo a 76 columnas y se usa la codificación _entre comillas_ para conservar los saltos de línea. El tipo de contenido depende de los caracteres que se encuentren en el texto del mensaje, de la siguiente manera: 
  
- Si solo se encuentran caracteres de 7 bits y ninguna línea supera los 140 caracteres de longitud, el mensaje es texto ASCII. _Content-Type: text/plain; charset = US-ASCII_ (Se presupone Content-Transfer-Encoding = 7). 
    
- Si se encuentran líneas largas o caracteres de 8 bits, el mensaje es texto y el juego de caracteres lo determina la configuración regional. Debe elegirse a partir de los juegos de caracteres definidos por la norma ISO 8859. _Content-Type: text/plain; charset = ISO-8859-1_ (u otro juego de caracteres válido) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Para los mensajes MIME entrantes, si la parte de contenido del primer mensaje tiene _tipo de contenido\* : Text/_ (es decir, cualquier tipo de texto) y se reconoce su juego de caracteres, se asigna a **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Una parte de contenido del primer mensaje que no cumple este criterio se convierte en datos adjuntos. Las partes subsiguientes también se convierten en datos adjuntos.
  
En el modo uuencode, el texto del mensaje en los mensajes salientes se ajusta a 78 columnas, como en el caso de MS Mail 3. x. El tipo de contenido es "text/plain". Para conservar los saltos de párrafo del mensaje original en estas circunstancias, observe las siguientes convenciones en el texto ajustado. Hay tres razones posibles para finalizar una línea de texto, cada una con su propia secuencia de caracteres:
  
- Salto de línea. El texto original contenía una nueva línea introducida por el usuario (marca de párrafo). En el transporte, se asigna a una línea nueva sin espacios iniciales. Si el usuario escribe una nueva línea precedida por espacios en blanco, los espacios en blanco deben quitarse.
    
- Línea-nobreak. El texto original contenía una palabra demasiado tiempo para que quepa en una sola línea del mensaje. En el transporte, se asigna a una nueva línea precedida por dos espacios en blanco.
    
- Ajuste de línea. El texto original no contenía ninguna línea nueva, el texto es demasiado largo para caber en una sola línea del mensaje, pero puede dividirse entre dos palabras. En el transporte, se asigna a una nueva línea precedida de un solo espacio en blanco.
    

