---
title: THEMERESTORE (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Almacena el valor de formato local de una forma cuando se aplica un tema para que pueda restaurar el formato local si el usuario quita el tema posteriormente.
ms.openlocfilehash: f22f603cad1d310adc59d19e9b3e3882bd797fce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823409"
---
# <a name="themerestore-function"></a>Función THEMERESTORE

Almacena el valor de formato local de una forma cuando se aplica un tema para que pueda restaurar el formato local si el usuario quita el tema posteriormente.
  
## <a name="syntax"></a>Sintaxis

THEMERESTORE()
  
## <a name="example"></a>Ejemplo

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Restaura el formato de color de relleno local aplicado anteriormente a una forma si se elimina el tema actual.
  

