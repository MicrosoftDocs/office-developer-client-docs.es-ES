---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- dialogmsgproc (función) [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815527"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Este procedimiento está asociada con el cuadro de diálogo nativo de Windows muestra que [fShowDialog](fshowdialog.md) . Proporciona las rutinas de servicio llamadas por Windows para los eventos (mensajes) que se producen cuando el usuario opera uno de los botones del cuadro de diálogo, los campos de entrada o controles. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parámetros

 _hWndDlg_ (**HWND**)
  
Contiene el identificador de Windows de HWND del cuadro de diálogo.
  
 _mensaje_ (**UINT**)
  
El mensaje para responder a.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Argumentos que se pasan por parte de Windows.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

 **TRUE** si el mensaje procesado, **FALSE** si no. 
  
### <a name="example"></a>Ejemplo

Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones de la DLL genérica](functions-in-the-generic-dll.md)

