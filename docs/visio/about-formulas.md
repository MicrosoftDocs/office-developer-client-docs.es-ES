---
title: Fórmulas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: La clave para controlar las acciones de una forma es escribir las fórmulas que definen el comportamiento deseado. Puede modificar la fórmula de una celda para cambiar su valor y, en consecuencia, cambiar el comportamiento de la forma correspondiente. Por ejemplo, la celda Height de la sección de transformación de forma contiene una fórmula que puede cambiar para modificar el alto de la forma.
ms.openlocfilehash: 7df5ffe4d3dc32bcd5209bde353c39a92c7d422b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821482"
---
# <a name="about-formulas"></a>Información sobre fórmulas

La clave para controlar las acciones de una forma es escribir las fórmulas que definen el comportamiento deseado. Puede modificar la fórmula de una celda para cambiar su valor y, en consecuencia, cambiar el comportamiento de la forma correspondiente. Por ejemplo, la celda Height de la sección de transformación de forma contiene una fórmula que puede cambiar para modificar el alto de la forma.
  
Las fórmulas de Microsoft Visio son muy similares a las habituales en las hojas de cálculo. Visio considera todo el contenido de una celda como una fórmula, incluso si sólo es un valor numérico o una simple referencia a otra celda.
  
La fórmula de una celda puede heredarse de la celda equivalente de un patrón o estilo, o puede definirse localmente. Visio evalúa la fórmula y convierte el resultado en un valor adecuado para la celda, con las unidades correspondientes. En la ventana ShapeSheet, puede mostrar el contenido de las celdas como fórmulas o como valores.
  
## <a name="elements-of-a-formula"></a>Elementos de una fórmula

Una fórmula siempre comienza por un signo igual, que se inserta automáticamente. Una fórmula puede contener cualquiera de los elementos siguientes:
  
- Números
    
- Coordenadas
    
- Valores booleanos
    
- Operadores
    
- Funciones
    
- Cadenas
    
- Referencias a celdas
    
- Unidades de medida
    
## <a name="default-formulas"></a>Fórmulas predeterminadas

Al crear una forma, Visio crea fórmulas para ella de manera predeterminada. Para ver estas fórmulas predeterminadas, dibuje una forma simple (como un rectángulo, una elipse o una línea recta) y abra la ventana ShapeSheet (en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md), haga clic en **Mostrar ShapeSheet**).
  
## <a name="inherited-formulas"></a>Fórmulas heredadas

Visio utiliza la herencia de fórmulas siempre que es posible. En lugar de hacer una copia local de cada fórmula de la instancia, ésta hereda fórmulas de su patrón en la galería de símbolos de documento y hereda el formato de la definición de estilo almacenada con el dibujo. Así los archivos son más pequeños y, además, los cambios en las fórmulas del patrón o en la definición del estilo se propagan a todas las instancias.
  
Las fórmulas heredadas aparecen en las celdas con texto negro.
  
## <a name="local-formulas"></a>Fórmulas locales

Al escribir una fórmula local para una instancia, reemplazará la fórmula heredada en la celda por otra que la suplanta. Los cambios posteriores a la celda en el patrón o el estilo no afectarán a esta instancia, porque con la fórmula local se ha bloqueado la herencia para esa celda.
  
Al aplicar un estilo se eliminan todas las fórmulas locales de las celdas relacionadas a menos que use la función GUARD para protegerlas.
  
El texto azul indica que la fórmula es local, como resultado de modificar la fórmula en la ventana ShapeSheet o por algún cambio en la forma que haya causado que Visio cambie la fórmula de esa celda.
  
## <a name="automatic-updates-to-formulas"></a>Actualizaciones automáticas de las fórmulas

 Visio actualiza automáticamente algunas celdas cuando se cambia una forma en un dibujo. Esto significa que, en algunas circunstancias, las fórmulas que escriba pueden ser reemplazadas. Por ejemplo, si arrastra el controlador de una esquina para cambiar el tamaño de una forma, Visio restablece las fórmulas de las celdas PinX, PinY, Width y Height. 
  
Si es necesario, puede proteger las fórmulas para evitar cambios mediante la función GUARD.
  

