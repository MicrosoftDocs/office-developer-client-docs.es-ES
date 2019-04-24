---
title: Función THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Devuelve un valor RGB o un entero que representa un índice en la paleta de colores del documento, donde el color (número) que se pasa como argumento ha sido modificado por el valor de matiz o sombreado especificado que se ha guardado en la configuración de degradado del tema activo.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332266"
---
# <a name="themecbv-function"></a>Función THEMECBV

Devuelve un valor RGB o un entero que representa un índice en la paleta de colores del documento, donde el color (número) que se pasa como argumento ha sido modificado por el valor de matiz o sombreado especificado que se ha guardado en la configuración de degradado del tema activo. 
  
## <a name="version-information"></a>Información de versiones

Versión añadida: Visio 2013
 
  
## <a name="syntax"></a>Sintaxis

 **THEMECBV** ( _color_, _gradient_stop_number_)
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Number** <br/> |Un número que representa un índice en la paleta de colores del documento.  <br/> |
| _gradient_stop_number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El punto de degradado (tinta o sombreado) almacenado en la configuración de degradado del tema activo para aplicar al color.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

 **Number**
  
## <a name="remarks"></a>Comentarios

> [!NOTE]
> La función THEMECBV no realiza ninguna acción en el color que se pasa como argumento si el QuickStyle que se asigna a la forma no tiene degradado. 
  
La configuración del degradado en un tema es una serie de puntos de degradado numerados que corresponden a una "iluminación" (tono) o "oscurecer" (sombreado). Estas tonalidades y matices se aplican a un color base para crear un efecto de color degradado.
  
La función **THEMECBV** toma una entrada en color y envía el color después de haber sido modificada por la tinta o sombra del punto de degradado especificado. Las tintas y los tonos proceden de la definición del tema si el estilo rápido actual contiene un relleno degradado. Si el estilo rápido activo no especifica un relleno degradado o la forma se establece en sin tema, esta fórmula simplemente devuelve el color que se ha pasado para el primer argumento. 
  
## <a name="example"></a>Ejemplo

 `THEMECBV(FillForegnd, 5)`
  
Devuelve el color creado aplicando la tinta o el sombreado del quinto punto de degradado del degradado al color especificado en la celda **FillForegnd** . 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Devuelve un tono o tono de rojo creado aplicando el segundo punto de degradado a un color base de rojo.
  

