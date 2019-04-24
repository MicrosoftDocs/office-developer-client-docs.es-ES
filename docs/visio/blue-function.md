---
title: BLUE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Devuelve el componente azul de un color. El valor devuelto es un número entero comprendido entre 0 y 255, ambos inclusive. La función devuelve 0 para la entrada no válida.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297357"
---
# <a name="blue-function"></a>Función BLUE

Devuelve el componente azul de un color. El valor devuelto es un número entero comprendido entre 0 y 255, ambos inclusive. La función devuelve 0 para la entrada no válida.
  
## <a name="syntax"></a>Sintaxis

AZUL (* * *expresión* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="example-1"></a>Ejemplo 1

AZUL (hoja. 4! FillForegnd
  
Devuelve el componente azul del color de relleno del primer plano en la Hoja.4.
  
## <a name="example-2"></a>Ejemplo 2

AZUL (13)
  
Devuelve 128 si el documento utiliza la paleta predeterminada de colores de Visio, en la que el índice 13 está asignado al color cian.
  
## <a name="example-3"></a>Ejemplo 3

BLUE(RGB(10; 20; 30))
  
Devuelve 30.
  

