---
title: THEMEGUARD (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protege las celdas de formato de una forma para asegurarse de que usan los aspectos apropiados del tema actual.
ms.openlocfilehash: 10a7772995b9cc22e53ff577b2f663d7c97d0816
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823396"
---
# <a name="themeguard-function"></a>Función THEMEGUARD

Protege las celdas de formato de una forma para asegurarse de que usan los aspectos apropiados del tema actual.
  
## <a name="syntax"></a>Sintaxis

THEMEGUARD()
  
## <a name="remarks"></a>Observaciones

Aplica la función THEMEGUARD a una celda no se protege el formato manual de la misma manera que hace función aplicar la protección. Si se aplica formato a la forma en la interfaz de usuario o mediante programación, mediante la automatización, se reemplaza la fórmula THEMEGUARD, a menos que incluya la función SETATREFEXPR en la fórmula para almacenar el valor de formato manual. 
  
## <a name="example"></a>Ejemplo

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Especifica que la forma toma el color de énfasis 2 del tema actual, en vez del color de relleno principal del tema.
  

