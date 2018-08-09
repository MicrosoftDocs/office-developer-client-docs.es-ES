---
title: SETATREF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Redirige valores actualizados resultantes de acciones de la interfaz de usuario (UI) o la automatización a otra celda.
ms.openlocfilehash: 69a9cb93ae3fbd807ef4f306be386f5389a6cfeb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823125"
---
# <a name="setatref-function"></a>Función SETATREF

Redirige valores actualizados resultantes de acciones de la interfaz de usuario (UI) o la automatización a otra celda. 
  
## <a name="syntax"></a>Sintaxis

SETATREF (** *referencia* ** [, ** *expresión_conjunto* ** [, ** *omitir_eval* **]]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _referencia_ <br/> |Obligatorio  <br/> |**String** <br/> |Referencia a la celda adonde se redirigen las actualizaciones.  <br/> |
| _expresión_conjunto_ <br/> |Opcional  <br/> |**String** <br/> |Una expresión que se asigna a la _referencia_.  <br/> |
| _omitir_eval_ <br/> |Opcional  <br/> |**Boolean** <br/> |Si es TRUE, la función SETATREF evalúa a (0) cero; Si es FALSE (valor predeterminado) la función SETATREF evalúa el valor de _referencia_.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando una acción del usuario en la ventana de dibujo o un método de automatización, hace que Microsoft Visio actualice una celda que contiene una fórmula SETATREF, el valor se redirige en su lugar a la celda referida por la fórmula SETATREF ( _referencia_). La fórmula de la celda que contiene la función SETATREF permanece intacta.
  
Si se omite _expresión_conjunto_ , el valor establecido en la interfaz de usuario o mediante la automatización se asigna a la celda referida; de lo contrario, el contenido de _expresión_conjunto_ se asigna a la celda que se hace referencia. Esto permite que el nuevo valor que se ha modificado o transforman antes de que se asigna a la celda que se hace referencia. 
  
La función SETATREF cuenta con dos funciones relacionadas: 
  
- La función SETATREFEXPR, que puede usar para representar el nuevo valor contenido en _expresión_conjunto_. Por ejemplo, una _expresión_conjunto_ SETATREFEXPR ()-2 en. podría usarse para restar 2 pulgadas desde el resultado SETATREFEXPR. 
    
- La función SETATREFEVAL, que se puede utilizar para indicar que algunas partes de _expresión_conjunto_ deben evaluadas y reemplazadas por el resultado. 
    
La función SETATREF está diseñada para su uso en las celdas que se puede cambiar por las acciones del usuario en la ventana de dibujo. Se admiten las celdas siguientes:
  
- Sección de transformación de forma: celdas Width, Height, Angle, PinX y PinY
    
- Sección de transformación de texto: celdas TxtWidth, TxtHeight, TxtAngle, TxtPinX y TxtPinY
    
- Sección de extremos 1D: celdas BeginX, BeginY, EndX y EndY
    
- Sección de controles: celdas Controls.X y Controls.Y
    
- Sección de datos de formas
    
Dado que SETATREF cambia la ubicación donde cambian los valores de celda, afecta al desencadenamiento de eventos. Si una celda contiene SETATREF, los eventos **FormulaChanged** y **CellChanged** se desencadenan para la celda que hace referencia SETATREF, no a la celda que contiene SETATREF. Si una celda que contiene SETATREF también contiene SETATREFEXPR, el evento **FormulaChanged** se desencadena también para la celda que contiene SETATREF debido a que se cambia un parámetro de función. 
  
A continuación se describen algunos puntos adicionales que conviene tener en cuenta al respecto de la función SETATREF:
  
- Las funciones SETATREF pueden encadenar hasta un máximo de 10 referencias a otras funciones SETATREF. 
    
- Las celdas pueden contener otras expresiones además de la función SETATREF, incluidas varias apariciones de SETATREF en una misma celda.
    
- Si las formas están pegadas, Visio sigue la cadena de referencias de SETATREF dentro de la misma hoja y coloca fórmulas de pegado en la celda referida. 
    
- La automatización reconoce la función SETATREF y sigue la cadena de celdas a las que se hace referencia. 
    
- Al igual que ocurre con GUARD, SETATREF no protege las celdas de los cambios realizados mediante la función SETF en ShapeSheet.
    
## <a name="example1"></a>Ejemplo 1

Supongamos que una forma posee una propiedad personalizada llamada Width, y la celda Width de la sección de transformación de forma contiene la siguiente fórmula:
  
=SETATREF(Prop.Width)
  
Si un usuario cambiar el ancho de la forma en la interfaz de usuario, el nuevo valor se asigna a la celda Prop.Width, no a la celda Width de la sección transformación de forma; la fórmula de la celda Width permanece inalterada. También puede establecer el ancho de la forma mediante el uso de datos de formas.
  
## <a name="example2"></a>Example2

Las soluciones de Visio suelen contar con formas relacionadas jerárquicamente, y así se precisa que las formas secundarias se muevan cuando lo hace una principal. A continuación se muestra un ejemplo de cómo se puede administrar esta relación con la función SETATREF en ShapeSheet. 
  
Las siguientes fórmulas se encuentran en la sección de transformación de formas de la forma secundaria. Además, definimos unas celdas de usuario llamadas Usuario.DeltaX y Usuario.DeltaY, que rastrean la cota de desplazamiento de ParentShape. Esto permite a la forma secundaria moverse cuando lo hace la principal, además de preservar la jerarquía si se mueve la secundaria.
  
PinX =SETATREF(Usuario.DeltaX; SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(Usuario.DeltaY; SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
Cuando la forma secundaria se mueve mediante la interfaz de usuario, los nuevos valores de PinX y PinY se establecen como el parámetro de la función SETATREFEXPR. La función SETATREF evalúa la fórmula encerrada en SETATREFEVAL y reemplaza PinX y PinY con sus resultados y, a continuación, la fórmula resultante se asigna a las celdas de usuario que se hace referencia en el function—User.DeltaX SETATREF y usuario.DeltaY. Por último, los valores devueltos por SETATREF (usuario.DeltaX y usuario.DeltaY) se agregan a la ubicación del pin de ParentShape para calcular la ubicación del pin de la forma secundaria.
  

