---
title: SETATREFEXPR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Almacena un valor que se establece a través de una acción de la interfaz de usuario (UI) o la automatización.
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823142"
---
# <a name="setatrefexpr-function"></a>Función SETATREFEXPR

Almacena un valor que se establece a través de una acción de la interfaz de usuario (UI) o la automatización.
  
## <a name="syntax"></a>Sintaxis

SETATREFEXPR ([** *expr_opc* **]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expr_opc_ <br/> |Opcional  <br/> |**Varían** <br/> |Una expresión que se ha reemplazado por el valor o expresión que se va a asignar a la celda que se hace referencia en la función SETATREF. Si no se indica, su valor inicial es 0 (cero).  <br/> |
   
## <a name="remarks"></a>Observaciones

El valor de una expresión SETATREFEXPR también se puede establecer desde una función SETATREF en otra celda que haga referencia a la celda que contiene la expresión SETATREFEXPR. 
  
No está limitado al uso de la función SETATREFEXPR como un parámetro a la función SETATREF. 
  
## <a name="example-1"></a>Ejemplo 1

En el ejemplo siguiente, se usa la función SETATREFEXPR para garantizar que una forma tiene el ancho de su texto.
  
Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())
  
## <a name="example-2"></a>Ejemplo 2

En el ejemplo siguiente, se muestra cómo utilizar la función SETATREFEXPR para que las formas se ajusten a una cuadrícula personalizada. Las fórmulas SETATREFEXPR se colocan en las celdas PinX y PinY, lo cual produce que el eje de la forma se ajuste a la cuadrícula definida en User.GridX y User.GridY. 
  
User.GridX =2 pda
  
User.GridY =2 pda
  
PinX = INT (SETATREFEXPR () / User.GridX +.5)\*User.GridX
  
PinY = INT (SETATREFEXPR () / User.GridY +.5)\*User.GridY
  
## <a name="example-3"></a>Ejemplo 3

Para conocer un ejemplo sobre el uso de la función SETATREFEXPR con la función SETATREF, vea el tema que trata la función [SETATREF](setatref-function.md). 
  

