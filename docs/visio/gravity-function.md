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
description: Calcula el ángulo correcto de un bloque de texto de rotación de la rotación de la forma indicada evitar que el texto quede hacia abajo.
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822241"
---
# <a name="gravity-function"></a>GRAVITY (función)

Calcula el ángulo correcto de un bloque de texto de rotación de la rotación de la forma indicada evitar que el texto quede hacia abajo.
  
## <a name="syntax"></a>Sintaxis

GRAVITY (** *ángulo* **, [** *límite 1* **], [** *límite 2* **]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _ángulo_ <br/> |Obligatorio  <br/> |**String** <br/> | Ángulo de la forma.  <br/> |
| _límite 1_ <br/> |Opcional  <br/> |**String** <br/> |Primer límite de rotación. El límite predeterminado es de 90 grados.  <br/> |
| _límite 2_ <br/> |Opcional  <br/> |**String** <br/> |Segundo límite de rotación. El límite predeterminado es de 270 grados.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Observaciones

La función GRAVITY se utiliza normalmente en la celda TxtAngle. 
  
El valor devuelto es 180 grados si _ángulo_ está comprendido entre los valores especificados mediante _límite 1_ y _límite 2_; en caso contrario, el valor devuelto es 0 grados.
  
La función normaliza automáticamente todos los argumentos para que estén comprendidos entre 0 y 360 grados. Si en un argumento no se especifican las unidades, se supone que se trata de radianes. 
  
## <a name="example-1"></a>Ejemplo 1

GRAVITY(ángulo)
  
Devuelve 180 grados si *ángulo* está comprendido entre 90 y 270 grados; de lo contrario, devuelve 0 grados. 
  
## <a name="example-2"></a>Ejemplo 2

GRAVITY(2)
  
Devuelve 180 grados, ya que 2 radianes es un valor angular comprendido entre 90 y 270 grados.
  
## <a name="example-3"></a>Ejemplo 3

GRAVITY(100 grad, 110 grad, 290 grad)
  
Devuelve 0 grados.
  
## <a name="example-4"></a>Ejemplo 4

GRAVITY(100 grad, 290 grad, 110 grad)
  
Devuelve 0 grados.
  

