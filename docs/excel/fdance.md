---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fdance (función) [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815637"
---
# <a name="fdance"></a>fDance

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Comando de ejemplo definida por el usuario que cambia las celdas seleccionadas en la hoja de cálculo activa alrededor hasta que el usuario presiona la **tecla ESC**. Cuando se carga GENERIC.xll, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Sintaxis

La función no toma ningún parámetro.
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

La función siempre devuelve 1.
  
## <a name="remarks"></a>Notas

Éste es un ejemplo de una operación larga. Llama a la función [xlAbort](xlabort.md) ocasionalmente. Esto da como resultado el procesador (ayudar con tareas cooperación) y comprueba si el usuario ha presionado la **tecla ESC** para cancelar la operación. Si es así, ofrece al usuario una oportunidad para cancelar la anulación. 
  
### <a name="example"></a>Ejemplo

Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función. 
  
## <a name="see-also"></a>Ver también



[Funciones en el archivo DLL genérica](functions-in-the-generic-dll.md)

