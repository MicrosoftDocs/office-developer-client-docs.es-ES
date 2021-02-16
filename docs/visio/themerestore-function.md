---
title: THEMERESTORE (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Almacena el valor de formato local de una forma cuando se aplica un tema para que pueda restaurar el formato local si el usuario quita posteriormente el tema.
ms.openlocfilehash: 628e246f91172f136dd1a70807fca2abc1ff5bdd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404291"
---
# <a name="themerestore-function"></a>Función THEMERESTORE

Almacena el valor de formato local de una forma cuando se aplica un tema para que pueda restaurar el formato local si el usuario quita posteriormente el tema.
  
## <a name="syntax"></a>Sintaxis

THEMIRSTORE()
  
## <a name="example"></a>Ejemplo

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Restaura el formato de color de relleno local aplicado anteriormente a una forma si se elimina el tema actual.
  

