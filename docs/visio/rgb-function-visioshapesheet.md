---
title: Función RGB (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Devuelve un valor que representa un índice en la paleta de colores del documento. Especifica un color por sus componentes rojo, verde y azul, donde cada uno es un número entre 0 y 255, ambos incluidos, o una expresión que da como resultado dicho número.
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426306"
---
# <a name="rgb-function-visioshapesheet"></a>Función RGB (VisioShapeSheet)

Devuelve un valor que representa un índice en la paleta de colores del documento. Especifica un color por sus componentes rojo, verde y azul, donde cada uno es un número entre 0 y 255, ambos incluidos, o una expresión que da como resultado dicho número. 
  
## <a name="syntax"></a>Sintaxis

RGB(** *red* **, ** *green* **, ** *blue* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _rojo_ <br/> |Obligatorio  <br/> |**Number** <br/> |El componente rojo.  <br/> |
| _verde_ <br/> |Obligatorio  <br/> |**Number** <br/> |El componente verde.  <br/> |
| _azul_ <br/> |Obligatorio  <br/> |**Nmber** <br/> |El componente azul.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

Si el color que devuelve la función no forma parte de la paleta de colores del documento actual, se agrega.
  
La tabla siguiente muestra varios colores estándar y los valores de sus componentes rojo, verde y azul.
  
|**Color**|**Valor rojo**|**Valor verde**|**Valor azul**|
|:-----|:-----|:-----|:-----|
|Negro  <br/> |0  <br/> |0  <br/> |0  <br/> |
|Azul  <br/> |0  <br/> |0  <br/> |255  <br/> |
|Verde  <br/> |0  <br/> |255  <br/> |0  <br/> |
|Aguamarina  <br/> |0  <br/> |255  <br/> |255  <br/> |
|Rojo  <br/> |255  <br/> |0  <br/> |0  <br/> |
|Magenta  <br/> |255  <br/> |0  <br/> |255  <br/> |
|Amarillo  <br/> |255  <br/> |255  <br/> |0  <br/> |
|Blanco  <br/> |255  <br/> |255  <br/> |255  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

RGB(0,0,255)
  
Devuelve el índice del color azul.
  
## <a name="example-2"></a>Ejemplo 2

RGB(RED(Sheet.1! FillForegnd),120,0)
  
Devuelve el índice que corresponde a un color cuyo componente rojo coincide con el del relleno de primer plano en la Hoja.1.
  

