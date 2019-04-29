---
title: Celda ClippingPath (sección de información de imagen externa)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contiene una referencia a la geometría de la ruta de acceso con la que está rodeada una imagen.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425515"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>Celda ClippingPath (sección de información de imagen externa)

Contiene una referencia a la geometría de la ruta de acceso con la que está rodeada una imagen. 
  
## <a name="remarks"></a>Comentarios

Si la celda **ClippingPath** apunta a una ruta de acceso válida, la imagen se recorta para que la imagen se represente dentro de la ruta de acceso. Si la celda **ClippingPath** está vacía o contiene una entrada no válida, la imagen se representará con un clip rectangular, con los valores de escala y desplazamiento. 
  
> [!NOTE]
> Solo las rutas definidas por una sección de [geometría](geometry-section.md) en la ShapeSheet de la imagen son entradas válidas para la celda **ClippingPath** . Las referencias entre hojas no se pueden usar para definir una ruta de recorte de imagen. 
  
Para obtener una referencia a la celda **ClippingPath** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ClippingPath  <br/> |
   
Para obtener una referencia desde un programa a la celda **ClippingPath** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowForeign** <br/> |
| Índice de celda:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>Ejemplo

Puede cambiar la forma de delimitación de una imagen por una elipse de la siguiente manera:
  
- Inserte la imagen en el lienzo de dibujo.
    
- Haga clic con el botón secundario en la imagen y seleccione **Mostrar ShapeSheet**.
    
- Haga clic con el botón derecho en cualquier lugar de la ShapeSheet y seleccione **Insertar sección**.
    
- En el cuadro de diálogo **Insertar sección** , seleccione **geometría** y, a continuación, haga clic en **Aceptar**.
    
- En la sección nueva geometría (por ejemplo, "Geometry2"), elimine todas las filas menos una.
    
- Haga clic con el botón secundario en la fila restante y haga clic en **Cambiar tipo de fila**.
    
- En el cuadro de diálogo **Cambiar tipo de fila** , seleccione **elipse** y, a continuación, haga clic en **Aceptar**.
    
- En la sección **imagen externa** , establezca la fórmula de la celda **ClippingPath** en `="Geometry2.Path"` y, a continuación, acepte la fórmula. 
    

