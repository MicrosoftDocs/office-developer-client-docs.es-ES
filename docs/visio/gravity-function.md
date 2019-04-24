---
title: GRAVITY (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Calcula el ángulo de giro correcto del bloque de texto para la rotación de la forma indicada para evitar que el texto se gire hacia abajo.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360189"
---
# <a name="gravity-function"></a>Función GRAVITY

Calcula el ángulo de giro correcto del bloque de texto para la rotación de la forma indicada para evitar que el texto se gire hacia abajo.
  
## <a name="syntax"></a>Sintaxis

Gravity (* * *Angle* * *, [* * *límite1* * *], [* * *limit2* * *]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _respecto_ <br/> |Obligatorio  <br/> |**String** <br/> | Ángulo de la forma.  <br/> |
| _límite1_ <br/> |Opcional  <br/> |**String** <br/> |Primer límite de rotación. El límite predeterminado es de 90 grados.  <br/> |
| _limit2_ <br/> |Opcional  <br/> |**String** <br/> |Segundo límite de rotación. El límite predeterminado es de 270 grados.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

La función GRAVITY se utiliza normalmente en la celda TxtAngle. 
  
El valor devuelto es 180 grados si el _ángulo_ está comprendido entre los valores especificados por _límite1_ y _limit2_; de lo contrario, el valor devuelto es 0 grados.
  
La función normaliza automáticamente todos los argumentos para que estén comprendidos entre 0 y 360 grados. Si en un argumento no se especifican las unidades, se supone que se trata de radianes. 
  
## <a name="example-1"></a>Ejemplo 1

GRAVEDAD (ángulo)
  
Devuelve 180 grados si el *ángulo* está entre 90 y 270 grados; de lo contrario, devuelve 0 grados. 
  
## <a name="example-2"></a>Ejemplo 2

GRAVEDAD (2)
  
Devuelve 180 grados, ya que 2 radianes es un valor angular comprendido entre 90 y 270 grados.
  
## <a name="example-3"></a>Ejemplo 3

GRAVITY(100 grad, 110 grad, 290 grad)
  
Devuelve 0 grados.
  
## <a name="example-4"></a>Ejemplo 4

GRAVITY(100 grad, 290 grad, 110 grad)
  
Devuelve 0 grados.
  

