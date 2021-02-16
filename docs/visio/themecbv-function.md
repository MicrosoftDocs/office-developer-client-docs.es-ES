---
title: Función THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Devuelve un valor RGB o un entero que representa un índice en la paleta de colores del documento, donde el color (número) pasado como argumento ha sido modificado por el valor de tono o tono especificado almacenado en la configuración de degradado del tema activo.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429141"
---
# <a name="themecbv-function"></a>Función THEMECBV

Devuelve un valor RGB o un entero que representa un índice en la paleta de colores del documento, donde el color (número) pasado como argumento ha sido modificado por el valor de tono o tono especificado almacenado en la configuración de degradado del tema activo. 
  
## <a name="version-information"></a>Información de versiones

Versión añadida: Visio 2013
 
  
## <a name="syntax"></a>Sintaxis

 **THEMECBV**( _color_,  _gradient_stop_number_)
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Number** <br/> |Número que representa un índice en la paleta de colores del documento.  <br/> |
| _gradient_stop_number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El punto de degradado (tono o sombra) almacenado en la configuración de degradado del tema activo que se aplicará al color.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

 **Number**
  
## <a name="remarks"></a>Comentarios

> [!NOTE]
> La función THEMECBV no hace nada con el color pasado como argumento si el QuickStyle asignado a la forma no tiene un degradado. 
  
La configuración de degradado de un tema es una serie de delimitadores de degradado numerados que corresponden a una "iluminación" (tono) o "oscurecido" (sombra). Estos tonos y tonos se aplican a un color base para crear un efecto de color degradado.
  
La **función THEMECBV** toma una entrada de color y genera el color después de que haya sido modificado por el tono o la sombra del delimitador de degradado especificado. Los tonos y sombras provienen de la definición del tema, si el estilo rápido actual contiene un relleno degradado. Si el estilo rápido activo no especifica un relleno degradado o la forma está establecida en Sin tema, esta fórmula simplemente devuelve el color que se pasó para el primer argumento. 
  
## <a name="example"></a>Ejemplo

 `THEMECBV(FillForegnd, 5)`
  
Devuelve el color creado aplicando el tono o la sombra del quinto punto de degradado del degradado al color especificado en la celda **FillForegnd.** 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Devuelve una sombra o tono de rojo creado aplicando el segundo punto de degradado a un color base de rojo.
  

