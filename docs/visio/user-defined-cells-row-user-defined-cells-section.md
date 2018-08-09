---
title: Fila User-defined Cells (Sección de celdas definidas por el usuario)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
localization_priority: Normal
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: Contiene el valor y la descripción de cada celda definida por el usuario en la solución. Una forma contiene una fila User-defined Cells por cada pareja de celdas Value/Prompt definida por el usuario.
ms.openlocfilehash: 45a9a033fe486a14e9881c3d79b79a129ecedc1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823485"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>Fila User-defined Cells (sección Celdas definidas por el usuario)

Contiene el valor y la descripción de cada celda definida por el usuario en la solución. Una forma contiene una fila User-defined Cells por cada pareja de celdas Value/Prompt definida por el usuario.
  
Filas de celdas definidas por el usuario son con nombre de usuario. *nombre* y contienen las celdas siguientes. Para obtener más información, vea los temas de la celda específica. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[Value](value-cell-user-defined-cells-section.md) <br/> |Especifica un valor para la correspondiente celda definida por el usuario.  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |Especifica un mensaje o comentario descriptivo para la celda definida por el usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las celdas definidas por el usuario se pueden utilizar para escribir fórmulas y constantes a las que hacen referencia otras celdas y herramientas complementarias. Los valores de las celdas definidas por el usuario son portátiles; es decir, si una fórmula que hace referencia a una celda definida por el usuario de una forma se copia en otra forma que no tiene la misma celda definida por el usuario, la celda se agrega a la forma.
  
 Puede agregar tantos usuarios.  *nombre* como sea necesario, asignar nombres descriptivos a las filas y establecer valores de celda. Para agregar una fila a una sección User-defined Cells existente, haga clic en una fila y haga clic en **Insertar fila** en el menú contextual. 
  
Puede hacer referencia a estas celdas por su nombre de fila, que aparece en la ventana ShapeSheet en texto de color rojo. Para asignar un nombre descriptivo para el usuario. *nombre* , haga clic en la fila y, a continuación, escriba un nombre como *desplazamiento* , por ejemplo, para crear el nombre de fila User.desplazamiento. A continuación, puede hacer referencia a la celda Prompt usando User.desplazamiento.Prompt. 
  
El nombre de fila que escriba debe ser único en la sección.
  

