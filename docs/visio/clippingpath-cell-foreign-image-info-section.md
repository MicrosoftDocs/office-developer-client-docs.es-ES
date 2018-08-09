---
title: Celda ClippingPath (sección Información de imagen externa)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contiene una referencia a la geometría de la ruta de acceso que está rodeada de una imagen.
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821762"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>Celda ClippingPath (sección Información de imagen externa)

Contiene una referencia a la geometría de la ruta de acceso que está rodeada de una imagen. 
  
## <a name="remarks"></a>Comentarios

Si la celda **ClippingPath** apunta a una ruta de acceso válida, la imagen se recorta para que se represente la imagen dentro de la ruta de acceso. Si la celda **ClippingPath** está vacía o contiene una entrada no válida, la imagen se representará con un clip rectangular, usando los valores de escala y desplazamiento. 
  
> [!NOTE]
> Sólo rutas de acceso definidas por una sección de [geometría](geometry-section.md) de ShapeSheet de la imagen son las entradas válidas de la celda **ClippingPath** . Referencias entre hojas no se puede usar para definir una ruta de acceso de recorte de imagen. 
  
Para obtener una referencia a la celda **ClippingPath** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ClippingPath  <br/> |
   
Para obtener una referencia a la celda **ClippingPath** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowForeign** <br/> |
| Índice de celda:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>Ejemplo

Puede cambiar la forma de límite de una imagen a un óvalo haciendo lo siguiente:
  
- Inserte la imagen en el lienzo de dibujo.
    
- Haga clic en la imagen y, a continuación, seleccione **Mostrar ShapeSheet**.
    
- El botón secundario en cualquier lugar de la hoja ShapeSheet y seleccione **Insertar sección**.
    
- En el cuadro de diálogo **Insertar sección** , seleccione la **geometría** y, a continuación, haga clic en **Aceptar**.
    
- En la sección de geometría nueva (por ejemplo, "Geometry2"), Eliminar fila todos menos uno.
    
- Haga clic en la fila restante y, a continuación, haga clic en **Cambiar tipo de fila**.
    
- En el cuadro de diálogo **Cambiar tipo de fila** , seleccione **elipse** y, a continuación, haga clic en **Aceptar**.
    
- En la sección **Foreign Image** , establezca la fórmula de la celda **ClippingPath** a `="Geometry2.Path"` y, a continuación, acepte la fórmula. 
    

