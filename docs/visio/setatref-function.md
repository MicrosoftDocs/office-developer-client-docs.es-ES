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
description: Redirige los valores actualizados resultantes de acciones en la interfaz de usuario (UI) o de automatización a otra celda.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326022"
---
# <a name="setatref-function"></a>Función SETATREF

Redirige los valores actualizados resultantes de acciones en la interfaz de usuario (UI) o de automatización a otra celda. 
  
## <a name="syntax"></a>Sintaxis

SETATREF (* * *referencia* * * [, * * *expresión_conjunto* * * [, * * *ignore_eval* * *]]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _reference_ <br/> |Obligatorio  <br/> |**String** <br/> |Referencia a la celda adonde se redirigen las actualizaciones.  <br/> |
| _expresión_conjunto_ <br/> |Opcional  <br/> |**String** <br/> |Expresión asignada a _referencia_.  <br/> |
| _ignore_eval_ <br/> |Opcional  <br/> |**Boolean** <br/> |Si es TRUE, la función SETATREF evalúa como (0) cero; Si FALSE (valor predeterminado), la función SETATREF da como resultado el valor de _referencia_.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando una acción de usuario en la ventana de dibujo, o un método de automatización, hace que Microsoft Visio actualice una celda que contiene una fórmula SETATREF, el valor se redirige en su lugar a la celda a la que se hace referencia mediante la fórmula SETATREF ( _referencia_). La fórmula de la celda que contiene la función SETATREF permanece intacta.
  
Si se omite _expresión_conjunto_ , el valor establecido en la interfaz de usuario o mediante la automatización se asigna a la celda a la que se hace referencia; de lo contrario, el contenido de _expresión_conjunto_ se asigna a la celda a la que se hace referencia. Esto permite modificar o transformar el nuevo valor antes de asignarlo a la celda de referencia. 
  
La función SETATREF cuenta con dos funciones relacionadas: 
  
- La función SETATREFEXPR, que puede usar para representar el nuevo valor en _expresión_conjunto_. Por ejemplo, un _expresión_conjunto_ de SETATREFEXPR ()-2 en. se puede usar para restar 2 pulgadas del resultado SETATREFEXPR. 
    
- La función SETATREFEVAL, que se puede usar para indicar que una parte de _expresión_conjunto_ debe evaluarse y reemplazarse por su resultado. 
    
La función SETATREF está diseñada para usarse en celdas que las acciones de usuario pueden cambiar en la ventana de dibujo. Se admiten las siguientes celdas:
  
- Sección de transformación de forma: celdas Width, Height, Angle, PinX y PinY
    
- Sección de transformación de texto: celdas TxtWidth, TxtHeight, TxtAngle, TxtPinX y TxtPinY
    
- Sección de extremos 1D: celdas BeginX, BeginY, EndX y EndY
    
- Sección de controles: celdas Controls.X y Controls.Y
    
- Sección de datos de formas
    
Dado que SETATREF cambia la ubicación donde cambian los valores de celda, afecta al desencadenamiento de eventos. Si una celda contiene SETATREF, los eventos **FormulaChanged** y **CellChanged** se desencadenan para la celda a la que hace referencia SETATREF, no para la que contiene SETATREF. Si una celda que contiene SETATREF también contiene SETATREFEXPR, el evento **FormulaChanged** se desencadena también para la celda que contiene SETATREF porque se cambia un parámetro de la función. 
  
A continuación se describen algunos puntos adicionales que conviene tener en cuenta al respecto de la función SETATREF:
  
- Las funciones SETATREF pueden encadenar hasta un máximo de 10 referencias a otras funciones SETATREF. 
    
- Las celdas pueden contener otras expresiones además de la función SETATREF, incluidas varias apariciones de SETATREF en una misma celda.
    
- Si las formas están pegadas, Visio sigue la cadena de referencias de SETATREF dentro de la misma hoja y coloca fórmulas de pegado en la celda referida. 
    
- La automatización reconoce la función SETATREF y sigue la cadena de celdas a las que se hace referencia. 
    
- Al igual que ocurre con GUARD, SETATREF no protege las celdas de los cambios realizados mediante la función SETF en ShapeSheet.
    
## <a name="example1"></a>Example1

Supongamos que una forma posee una propiedad personalizada llamada Width, y la celda Width de la sección de transformación de forma contiene la siguiente fórmula:
  
= SETATREF (prop. width)
  
Si un usuario va a cambiar el ancho de la forma en la interfaz de usuario, el nuevo valor se asigna a la celda prop. width, no a la celda width de la sección transformación; la fórmula de la celda width permanece inalterada. También es posible establecer el ancho de la forma mediante los datos de formas.
  
## <a name="example2"></a>Example2

Las soluciones de Visio suelen contar con formas relacionadas jerárquicamente, y así se precisa que las formas secundarias se muevan cuando lo hace una principal. A continuación se muestra un ejemplo de cómo se puede administrar esta relación con la función SETATREF en ShapeSheet. 
  
Las siguientes fórmulas se encuentran en la sección de transformación de formas de la forma secundaria. Además, definimos unas celdas de usuario llamadas Usuario.DeltaX y Usuario.DeltaY, que rastrean la cota de desplazamiento de ParentShape. Esto permite a la forma secundaria moverse cuando lo hace la principal, además de preservar la jerarquía si se mueve la secundaria.
  
PinX =SETATREF(Usuario.DeltaX; SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(Usuario.DeltaY; SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
Cuando se mueve la forma secundaria mediante la interfaz de usuario, los nuevos valores de PinX y PinY se establecen como el parámetro de la función SETATREFEXPR. La función SETATREF evalúa la fórmula incluida en SETATREFEVAL y reemplaza PinX y PinY con sus resultados y, a continuación, la fórmula resultante se asigna a las celdas de usuario a las que se hace referencia en la función SETATREF: User. DeltaX y User. DeltaY. Por último, los valores devueltos por SETATREF (User. DeltaX o User. DeltaY) se agregan a la ubicación del PIN de ParentShape para calcular la ubicación del PIN de la forma secundaria.
  

