---
title: Función THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Devuelve un valor RGB o un número entero que representa un índice en la paleta de colores del documento, donde el color (número) que se pasa como un argumento ha sido modificado por el valor especificado de tinta o sombreado almacenado en la configuración de degradado del tema activo.
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823403"
---
# <a name="themecbv-function"></a>Función THEMECBV

Devuelve un valor RGB o un número entero que representa un índice en la paleta de colores del documento, donde el color (número) que se pasa como un argumento ha sido modificado por el valor especificado de tinta o sombreado almacenado en la configuración de degradado del tema activo. 
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2013
 
  
## <a name="syntax"></a>Sintaxis

 **THEMECBV** ( _color_, _gradient_stop_number_)
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Número** <br/> |Un número que representa un índice en la paleta de colores del documento.  <br/> |
| _gradient_stop_number_ <br/> |Obligatorio  <br/> |**Número** <br/> |El punto de degradado (tinta o sombreado) almacenado en la configuración de degradado del tema activo que se debe aplicar al color.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

 **Número**
  
## <a name="remarks"></a>Comentarios

> [!NOTE]
> La función THEMECBV no modifica el color que se pasa como un argumento si la QuickStyle que se asigna a la forma no tiene un degradado. 
  
La configuración de degradado en un tema es una serie de puntos de degradado numeradas que correspondan a una "iluminado" (tint) o "oscurecimiento" (tono). Estos tonos y tintas se aplican a un color base para crear un efecto de color de degradado.
  
La función **THEMECBV** toma una entrada de color y da como resultado el color después de que se ha modificado por la tinta o sombreado del delimitador de degradado especificada. Los matices y gradaciones proceden de la definición del tema, si el estilo rápido actual contiene un relleno de degradado. Si no especifica el estilo rápido activo un relleno degradado o la forma se establece en Sin tema, esta fórmula devuelve simplemente el color que se pasó para el primer argumento. 
  
## <a name="example"></a>Ejemplo

 `THEMECBV(FillForegnd, 5)`
  
Devuelve el color creado mediante la aplicación de la tinta o sombreado en el punto de degradado quinto del degradado para el color especificado en la celda **FillForegnd** . 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Devuelve un tono o matiz de rojo creada aplicando el segundo punto de degradado a un color base de rojo.
  

