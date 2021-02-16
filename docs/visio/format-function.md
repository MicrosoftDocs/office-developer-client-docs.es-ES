---
title: FORMAT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Devuelve el resultado de la expresión como una cadena con formato según formatpicture.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404655"
---
# <a name="format-function"></a>Función FORMAT

Devuelve el resultado de  _la expresión_ como una cadena con formato según  _formatpicture_.
  
## <a name="syntax"></a>Sintaxis

FORMAT(** *expression* **," ** *formatpicture* ** ") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor.  <br/> |
| _formatpicture_ <br/> |Obligatorio  <br/> |**String** <br/> |La imagen de formato usada para dar formato a la cadena.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

El tipo de la expresión y el especificado en el formato de imagen controlan el comportamiento de la cadena devuelta. El  _formatpicture_ debe ser apropiado para el tipo de expresión. Para obtener más información acerca de cómo especificar imágenes de formato, vea [Acerca del formato de imágenes.](about-format-pictures.md)
  
Devuelve un error si  el resultado de la expresión y el tipo esperado en _formatpicture_ son de otro tipo o si hay errores de sintaxis en _formatpicture_.
  
## <a name="example-1"></a>Ejemplo 1

FORMAT(1cm/4, "0,000 u")
  
Devuelve "0,250 cm".
  
## <a name="example-2"></a>Ejemplo 2

FORMAT(1cm/4, "0,00 U")
  
Devuelve "0,25 CM".
  
## <a name="example-3"></a>Ejemplo 3

FORMAT(1cm/4, "0,0 u")
  
Devuelve "0,3 cm".
  

