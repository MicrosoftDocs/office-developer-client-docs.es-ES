---
title: THEMEGUARD (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protege las celdas de formato de una forma para asegurarse de que usan los aspectos adecuados del tema actual.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404949"
---
# <a name="themeguard-function"></a>Función THEMEGUARD

Protege las celdas de formato de una forma para asegurarse de que usan los aspectos adecuados del tema actual.
  
## <a name="syntax"></a>Sintaxis

THEMEGUARD()
  
## <a name="remarks"></a>Comentarios

Si se aplica la función THEMEGUARD a una celda, no se protege el formato manual de la misma forma que si se aplicase la función GUARD. Si aplica formato a la forma en la interfaz de usuario o mediante programación, mediante automatización, se invalida la fórmula THEMEGUARD, a menos que incluya la función SETATREFEXPR en la fórmula para almacenar el valor de formato manual. 
  
## <a name="example"></a>Ejemplo

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Especifica que la forma toma el color de énfasis 2 del tema actual, en vez del color de relleno principal del tema.
  

