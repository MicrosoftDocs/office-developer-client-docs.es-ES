---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- función dialogmsgproc [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1de1b73f5672067f07518ef3367d77349395a1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406517"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Este procedimiento está asociado con el cuadro Windows de diálogo nativo que [fShowDialog](fshowdialog.md) muestra. Proporciona las rutinas de servicio llamadas por Windows para los eventos (mensajes) que se producen cuando el usuario opera uno de los botones, campos de entrada o controles del cuadro de diálogo. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parameters

 _hWndDlg_ (**HWND**)
  
Contiene el identificador de Windows HWND del cuadro de diálogo.
  
 _message_ (**UINT**)
  
Mensaje al que responder.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Argumentos pasados por Windows.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

 **TRUE** si se procesa el mensaje, **FALSE** si no es así. 
  
### <a name="example"></a>Ejemplo

Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

