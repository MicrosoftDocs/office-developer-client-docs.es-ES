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
  
Para los mensajes salientes en modo MIME, el tipo de contenido depende de si hay datos adjuntos y de cómo es el texto del mensaje. Si hay datos adjuntos, el tipo de contenido es  _multiparte/mixto;_ el texto del mensaje y cada dato adjunto se convierten en una parte independiente del contenido del mensaje, cada uno con su propio tipo de contenido. Si no hay datos adjuntos, el tipo de contenido del mensaje es  _texto/sin_ formato y solo hay una parte. 
  
El texto del mensaje no está ajustado en línea a menos que alguna línea supere los 140 caracteres de longitud. Si lo hace, todo el texto se ajusta  a 76 columnas y la codificación imprimible entre comillas se usa para conservar saltos de línea. El tipo de contenido depende de los caracteres que se encuentran en el texto del mensaje, como se indica a continuación: 
  
- Si solo se encuentran caracteres de 7 bits y ninguna línea supera los 140 caracteres de longitud, el mensaje es texto ASCII. _Tipo de contenido: texto/sin formato; charset=us-ascii_ (se asume Content-Transfer-Encoding=7bit). 
    
- Si se encuentran líneas largas o caracteres de 8 bits, el mensaje es texto y el juego de caracteres lo determina la configuración regional. Debe elegirse entre los conjuntos de caracteres definidos por la norma ISO 8859. _Tipo de contenido: texto/sin formato; charset=iso-8859-1_ (u otro conjunto de caracteres válido) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Para los mensajes MIME entrantes, si el primer elemento de contenido del mensaje tiene tipo _content: \* text/_ (es decir, cualquier tipo de texto) y se reconoce su juego de caracteres, se asigna **a PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Un primer elemento de contenido de mensaje que no cumple este criterio se convierte en datos adjuntos. Las partes posteriores también se convierten en datos adjuntos.
  
En el modo uuencode, el texto del mensaje de los mensajes salientes se ajusta en línea a 78 columnas, como en MS Mail 3.x. El tipo de contenido es "texto/sin formato". Para conservar los saltos de párrafo del mensaje original en estas circunstancias, observe las convenciones siguientes en el texto ajustado. Hay tres razones posibles para terminar una línea de texto, cada una con su propia secuencia de caracteres:
  
- Salto de línea. El texto original contenía una nueva línea especificada por el usuario (marca de párrafo). En el transporte, se asigna a una nueva línea sin espacios en blanco anteriores. Si el usuario escribe una nueva línea precedida de espacios en blanco, los espacios en blanco deben quitarse.
    
- Line-nobreak. El texto original contenía una palabra demasiado larga para caber en una sola línea del mensaje. En el transporte, se asigna a una nueva línea precedida de dos espacios en blanco.
    
- Ajuste de línea. El texto original no contenía ninguna línea nueva, el texto es demasiado largo para caber en una sola línea del mensaje, pero se puede dividir entre dos palabras. En el transporte, se asigna a una nueva línea precedida de un solo espacio en blanco.
    

