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
description: Almacena un valor que se establece a través de una acción en la interfaz de usuario (UI) o automatización.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326008"
---
# <a name="setatrefexpr-function"></a>Función SETATREFEXPR

Almacena un valor que se establece a través de una acción en la interfaz de usuario (UI) o automatización.
  
## <a name="syntax"></a>Sintaxis

SETATREFEXPR ([* * *expr_opt* * *]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |Opcional  <br/> |**Diferencias** <br/> |Expresión que se reemplaza por el valor o la expresión que se asigna a la celda a la que se hace referencia en la función SETATREF. Si no se indica, su valor inicial es 0 (cero).  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de una expresión SETATREFEXPR también se puede establecer desde una función SETATREF en otra celda que haga referencia a la celda que contiene la expresión SETATREFEXPR. 
  
No está limitado a usar la función SETATREFEXPR como un parámetro para la función SETATREF. 
  
## <a name="example-1"></a>Ejemplo 1

En el ejemplo siguiente, se usa la función SETATREFEXPR para garantizar que una forma tiene el ancho de su texto.
  
Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())
  
## <a name="example-2"></a>Ejemplo 2

En el ejemplo siguiente, se muestra cómo utilizar la función SETATREFEXPR para que las formas se ajusten a una cuadrícula personalizada. Las fórmulas SETATREFEXPR se colocan en las celdas PinX y PinY, lo cual produce que el eje de la forma se ajuste a la cuadrícula definida en User.GridX y User.GridY. 
  
User.GridX =2 pda
  
User.GridY =2 pda
  
PinX = INT (SETATREFEXPR ()/User.GridX + 5)\*User. GridX
  
PinY = INT (SETATREFEXPR ()/User.GridY + 0,5)\*User. GridY
  
## <a name="example-3"></a>Ejemplo 3

Para conocer un ejemplo sobre el uso de la función SETATREFEXPR con la función SETATREF, vea el tema que trata la función [SETATREF](setatref-function.md). 
  

