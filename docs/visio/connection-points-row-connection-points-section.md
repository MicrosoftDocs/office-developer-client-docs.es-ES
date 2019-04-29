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
description: Contiene las coordenadas x e y, la dirección horizontal y vertical y el tipo de un único punto de conexión de una forma. Las coordenadas de los puntos de conexión se miden desde el origen de la forma. Una forma contiene una fila Puntos de conexión por cada punto de conexión.
ms.openlocfilehash: 301ea4fb446d9acafd4b59af388c3e7b2d419e20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415512"
---
# <a name="connection-points-row-connection-points-section"></a>Fila Puntos de conexión (Sección de puntos de conexión)

Contiene las coordenadas *x* e ** y, la dirección horizontal y vertical y el tipo de un único punto de conexión de una forma. Las coordenadas de los puntos de conexión se miden desde el origen de la forma. Una forma contiene una fila Puntos de conexión por cada punto de conexión. 
  
Si se asignan nombres a las filas Puntos de conexión, esos nombres aparecerán como Connections. *nombre* en la ventana ShapeSheet. Las filas Puntos de conexión contienen las celdas siguientes. Para obtener más detalles, vea los temas de Ayuda acerca de la celda específica. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |Coordenada *x* de un punto de conexión en coordenadas locales.  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |La coordenada *y* de un punto de conexión en coordenadas locales.  <br/> |
|[Celda DirX/A](dirxa-cell-connection-points-section.md) <br/> |El componente *x* para el vector de alineación necesario de un punto de conexión coincidentes. También se utiliza para orientar el segmento adjunto de un conector dinámico. Esta celda acepta valores de punto flotante.  <br/> |
|[Celda DirY/B](diryb-cell-connection-points-section.md) <br/> |El componente *y* para el vector de alineación necesario de un punto de conexión coincidentes. También se utiliza para orientar el segmento adjunto de un conector dinámico. Esta celda acepta valores de punto flotante.  <br/> |
|[Tipo/C](typec-cell-connection-points-section.md) <br/> |Tipo del punto de conexión (0 = entrante; 1 = saliente; 2 = entrante y saliente).  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |Celda de borrador que se puede utilizar para escribir o probar fórmulas. Para obtener acceso a esta celda, haga clic con el botón secundario en una fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las celdas de la fila Connections. la fila de *nombre* tiene la etiqueta DirX/A, DirY/B y Type/C porque estas filas pueden ser filas extendidas o no extendidas. 
  
La mayor parte de los puntos de conexión (todos los puntos de conexión creados desde la interfaz de usuario) son no extendidos y tienen celdas DirX, DirY y Type. Su tipo de fila es **visTagCnnctPt** o **visTagCnnctNamed.**
  
En filas no extendidas, las celdas DirX y DirY definen conjuntamente un vector de dirección que influye en el giro de las formas involucradas en las conexiones que utilizan el punto de conexión. Si ambas son cero, el punto no tiene dirección. Los puntos de conexión son de los tipos siguientes:
  
- Entrante (0), que significa que la forma se pega a ellos. Éste es el valor predeterminado.
    
- Saliente (1), que significa que estos puntos de conexión se pegarán a puntos de conexión entrantes.
    
- Entrante y saliente (2); en este caso la dirección es entrante, que se invierte si se utiliza como conexión saliente.
    
Las filas extendidas tienen celdas A, B, C y D, y se comportan como filas no extendidas sin dirección del tipo entrante. Las filas extendidas no se suelen utilizar, pero se podrían usar para asociar datos con un punto de conexión en las celdas A, B, C y D. Su tipo de fila es **visTagCnnctPtABCD** o **visTagCnnctNamedABCD**. Las filas extendidas se pueden identificar por la presencia de una fórmula en la celda D. 
  
 Puede agregar tantas filas Connections.  Asigne un *nombre* a las filas que necesite, asigne nombres descriptivos a las filas y establezca los valores de las celdas. Para agregar un punto de conexión a una sección de puntos de conexión existente, haga clic con el botón secundario en una fila y, después, haga clic en **Insertar fila** en el menú contextual. 
  
Puede hacer referencia a las celdas de las filas Puntos de conexión por su nombre de fila, que aparece en la ventana ShapeSheet como texto en color rojo. Para cambiar el nombre de la fila, haga clic en ella y, a continuación, escriba un nombre como *personalizado* , por ejemplo, para crear el nombre de fila Connections. Custom. Después, podrá hacer referencia a la celda X usando Connections.Personalizada.X, por ejemplo, o Connections.X1 si desea utilizar el número de la fila. 
  
El nombre de fila que escriba debe ser único en la sección. Cuando se crea un nombre para una fila en la sección de puntos de conexión, Microsoft Office Visio nombra todas las filas de la sección con el nombre predeterminado, Connections. Row_ *n* . 
  
Las filas Puntos de conexión con nombre no son compatibles con versiones de Visio anteriores a la 5.0. Cuando se guarda un archivo de dibujo de Visio que contiene filas Puntos de conexión con nombre en un formato anterior, las referencias a estas filas se convierten en referencias indizadas y se pierde su nombre.
  

