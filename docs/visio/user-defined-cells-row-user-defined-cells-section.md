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
ms.openlocfilehash: 01e2da8ef1e97e8a911df605ab6cf1e9f8a853eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337187"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>Fila User-defined Cells (Sección de celdas definidas por el usuario)

Contiene el valor y la descripción de cada celda definida por el usuario en la solución. Una forma contiene una fila User-defined Cells por cada pareja de celdas Value/Prompt definida por el usuario.
  
Las filas User-defined Cells se denominan User. *nombre* y contienen las celdas siguientes. Para obtener más detalles, vea los temas de Ayuda acerca de la celda específica. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[Valor](value-cell-user-defined-cells-section.md) <br/> |Especifica un valor para la correspondiente celda definida por el usuario.  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |Especifica un mensaje o comentario descriptivo para la celda definida por el usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las celdas definidas por el usuario se pueden utilizar para escribir fórmulas y constantes a las que hacen referencia otras celdas y herramientas complementarias. Los valores de las celdas definidas por el usuario son portátiles; es decir, si una fórmula que hace referencia a una celda definida por el usuario de una forma se copia en otra forma que no tiene la misma celda definida por el usuario, la celda se agrega a la forma.
  
 Puede agregar tantas filas User.  Asigne un *nombre* a las filas que necesite, asigne nombres descriptivos a las filas y establezca los valores de las celdas. Para agregar una fila a una sección existente de celdas definidas por el usuario, haga clic con el botón secundario en una fila y, después, haga clic en **Insertar fila** en el menú contextual. 
  
Puede hacer referencia a estas celdas por su nombre de fila, que aparece en la ventana ShapeSheet como texto en color rojo. Para asignar un nombre descriptivo a una fila User. *nombre* filas, haga clic en la fila y, a continuación, escriba un nombre como *desplazamiento* , por ejemplo, para crear el nombre de fila User. offset. Después, podrá hacer referencia a la celda Prompt usando User.Desplazamiento.Prompt. 
  
El nombre de fila que escriba debe ser único en la sección.
  

