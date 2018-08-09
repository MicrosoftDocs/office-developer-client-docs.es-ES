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
ms.openlocfilehash: 9dba148646678f0740c5b2c338ae345ecd76dfac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818393"
---
# <a name="message-text"></a>Texto del mensaje

  
  
**Hace referencia a**: Outlook 
  
Para los mensajes salientes en el modo de MIME, el tipo de contenido depende de si hay datos adjuntos y qué aspecto tiene el texto del mensaje. Si hay datos adjuntos, el tipo de contenido es _multipart/mixed;_ el texto del mensaje y los datos adjuntos se convierten en una parte independiente del contenido del mensaje, cada uno con su propio tipo de contenido. Si no hay ningún datos adjuntos, el tipo de contenido del mensaje es _texto sin formato_ y hay sólo una parte. 
  
El texto del mensaje no es línea-ajustado a menos que algunas línea supera 140 caracteres de longitud. Si lo hace, todo el texto se ajusta a las 76 columnas y el _Entrecomillado imprimible_ codificación se utiliza para conservar los saltos de línea. El tipo de contenido depende de los caracteres que se encuentran en el texto del mensaje, como se indica a continuación: 
  
- Si sólo se encuentran caracteres de 7 bits y línea no supera 140 caracteres de longitud, el mensaje es texto ASCII. _Content-type: texto sin formato; charset = us-ascii_ (Content-Transfer-Encoding = 7 bits se supone.) 
    
- Si se encuentran las líneas largas o caracteres de 8 bits, el mensaje es texto y el juego de caracteres está determinado por la configuración regional. Se debe proceder de los conjuntos de caracteres definidos por ISO 8859 estándar. _Content-type: texto sin formato; charset = iso-8859-1_ (o en otro conjunto de caracteres válido) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Para los mensajes MIME entrantes, si el primer mensaje de elemento de contenido tiene _tipo de contenido: texto /\* _ (es decir, cualquier tipo de texto) y se reconoce su juego de caracteres, se asigna a **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Un primer elemento de contenido de mensaje no satisface este criterio se convierte en un archivo adjunto. Los elementos siguientes también se convierten en datos adjuntos.
  
En el modo de uuencode, texto del mensaje en los mensajes salientes es línea ajustado a 78 columnas, en cuanto a Microsoft Mail 3.x. El tipo de contenido es "text/plain". Para conservar los saltos de párrafo del mensaje original en estas circunstancias, tenga en cuenta las siguientes convenciones en el texto ajustado. Existen tres razones posibles para finalizar una línea de texto, cada uno con su propia secuencia de caracteres:
  
- Salto de línea. El texto original contiene una línea nueva que ha escrito el usuario (marca de párrafo). En el transporte, se asigna a una nueva línea con sin espacios en blanco anteriores. Si el usuario escribe una nueva línea precedida por espacios en blanco, deben se eliminan los espacios en blanco.
    
- Línea-nobreak. El texto original contiene una palabra demasiado larga para caber en una sola línea del mensaje. En el transporte, se asigna a una nueva línea precedida por dos espacios en blanco.
    
- Ajuste de línea. El texto original no incluido ninguna nueva línea, el texto es demasiado largo para caber en una sola línea del mensaje, pero puede ser rota entre dos o más palabras. En el transporte, se asigna a una nueva línea precedida por un espacio en blanco.
    

