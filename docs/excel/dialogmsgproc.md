---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- función dialogmsgproc [Excel 2007]
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
  
Este procedimiento está asociado con el cuadro de diálogo de Windows nativo que [fShowDialog](fshowdialog.md) muestra. Proporciona las rutinas de servicio llamadas por Windows para los eventos (mensajes) que se producen cuando el usuario opera uno de los botones, los campos de entrada o los controles del cuadro de diálogo. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parameters

 _hWndDlg_ (**HWnd**)
  
Contiene el identificador de ventana de HWND del cuadro de diálogo.
  
 _mensaje de error_ (**Uint**)
  
Mensaje al que responde.
  
 _wParam_ (**WParam**)
  
 _lParam_ (**LParam**)
  
Argumentos pasados por Windows.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

 **True** si el mensaje se procesa, **false** en caso contrario. 
  
### <a name="example"></a>Ejemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función. 
  
## <a name="see-also"></a>Ver también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

