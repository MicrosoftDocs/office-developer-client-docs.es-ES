---
title: Fila Puntos de conexión (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3005
localization_priority: Normal
ms.assetid: eaac62a5-f516-9b81-587a-8e0e02de59ee
description: Contiene x - e y-coordenadas, dirección horizontal y vertical y tipo de una sola conexión punto de una forma. Coordenadas de puntos de conexión se miden desde el origen de la forma. Una forma contiene una fila de puntos de conexión para cada punto de conexión.
ms.openlocfilehash: f1b8daf7f9845b85e76020c7f89c8c42b4500823
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821847"
---
# <a name="connection-points-row-connection-points-section"></a>Fila Connection Points (sección Puntos de conexión)

Contiene el *x* - e *y* -coordenadas, dirección horizontal y vertical y tipo de una sola conexión punto de una forma. Coordenadas de puntos de conexión se miden desde el origen de la forma. Una forma contiene una fila de puntos de conexión para cada punto de conexión. 
  
Si se denominan filas puntos de conexión, esos nombres aparecerán como conexiones. *nombre* de la ventana ShapeSheet. Las filas puntos de conexión contienen las celdas siguientes. Para obtener más información, vea los temas de la celda específica. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |La *x* -coordenadas de un punto de conexión en coordenadas locales.  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |La *y* -coordenadas de un punto de conexión en coordenadas locales.  <br/> |
|[DirX/A](dirxa-cell-connection-points-section.md) <br/> |La *x* -component para el vector de alineación necesario de un punto de conexión coincidente. También se usa para orientar el segmento adjunto de un conector dinámico. Esta celda acepta flotante valor de punto.  <br/> |
|[DirY/B](diryb-cell-connection-points-section.md) <br/> |La *y* -component para el vector de alineación necesario de un punto de conexión coincidente. También se usa para orientar el segmento adjunto de un conector dinámico. Esta celda acepta flotante valor de punto.  <br/> |
|[Type/C](typec-cell-connection-points-section.md) <br/> |Tipo del punto de conexión (0 = entrante; 1 = saliente; 2 = entrante y saliente).  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |Celda en la que puede escribir o probar fórmulas. Para obtener acceso a esta celda, haga clic con el botón secundario del mouse (ratón) en la fila y, a continuación, haga clic en Cambiar tipo de fila en el menú contextual.<br/> |
   
## <a name="remarks"></a>Comentarios

Celdas en las conexiones. *nombre de la* fila están etiquetadas como DirX/A, DirY/B y Type/C porque pueden ser filas extendidas o no extendidas. 
  
La mayor parte de los puntos de conexión (todos los puntos de conexión creados desde la interfaz de usuario) son no extendidos y tienen celdas DirX, DirY y Type. Su tipo de fila es **visTagCnnctPt** o **visTagCnnctNamed.**
  
En filas no extendidas, las celdas DirX y DirY definen conjuntamente un vector de dirección que influye en el giro de las formas involucradas en las conexiones que utilizan el punto de conexión. Si ambas son cero, el punto no tiene dirección. Los puntos de conexión son de los tipos siguientes:
  
- Entrante (0), que significa que la forma se pega a ellos. Éste es el valor predeterminado.
    
- Saliente (1), que significa que estos puntos de conexión se pegarán a puntos de conexión entrantes.
    
- Entrante y saliente (2); en este caso la dirección es entrante, que se invierte si se utiliza como conexión saliente.
    
Las filas extendidas tienen celdas A, B, C y D, y se comportan como filas no extendidas sin dirección del tipo entrante. Las filas extendidas no se suelen utilizar, pero se podrían usar para asociar datos con un punto de conexión en las celdas A, B, C y D. Su tipo de fila es **visTagCnnctPtABCD** o **visTagCnnctNamedABCD**. Las filas extendidas se pueden identificar por la presencia de una fórmula en la celda D. 
  
 Puede agregar tantas conexiones.  *nombre* como sea necesario, asignar nombres descriptivos a las filas y establecer valores de celda. Para agregar un punto de conexión a una sección de puntos de conexión existente, haga clic en una fila y haga clic en **Insertar fila** en el menú contextual. 
  
Puede hacer referencia a celdas de la fila de puntos de conexión por su nombre de fila, que aparece en la ventana ShapeSheet en texto de color rojo. Para cambiar el nombre de la fila, haga clic en él y, a continuación, escriba un nombre como *personalizada* , por ejemplo, para crear el nombre de fila Connections.personalizada. A continuación, puede hacer referencia a la celda X usando Connections.personalizada.x, por ejemplo, o Connections.X1 si desea utilizar el número de fila. 
  
El nombre de fila que escriba debe ser único en la sección. Cuando se crea un nombre de fila en la sección de puntos de conexión, Microsoft Office Visio nombres de todas las filas de la sección con el nombre predeterminado, Connections.Row_ *n* . 
  
Las filas Puntos de conexión con nombre no son compatibles con versiones de Visio anteriores a la 5.0. Cuando se guarda un archivo de dibujo de Visio que contiene filas Puntos de conexión con nombre en un formato anterior, las referencias a estas filas se convierten en referencias indizadas y se pierde su nombre.
  

