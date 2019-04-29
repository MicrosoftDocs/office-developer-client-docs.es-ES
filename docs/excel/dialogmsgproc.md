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
# <a name="dialogmsgproc"></a><span data-ttu-id="d611c-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="d611c-104">DIALOGMsgProc</span></span>

<span data-ttu-id="d611c-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d611c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d611c-106">Este procedimiento está asociado con el cuadro de diálogo de Windows nativo que [fShowDialog](fshowdialog.md) muestra.</span><span class="sxs-lookup"><span data-stu-id="d611c-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="d611c-107">Proporciona las rutinas de servicio llamadas por Windows para los eventos (mensajes) que se producen cuando el usuario opera uno de los botones, los campos de entrada o los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d611c-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="d611c-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="d611c-108">Parameters</span></span>

 <span data-ttu-id="d611c-109">_hWndDlg_ (**HWnd**)</span><span class="sxs-lookup"><span data-stu-id="d611c-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="d611c-110">Contiene el identificador de ventana de HWND del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d611c-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="d611c-111">_mensaje de error_ (**Uint**)</span><span class="sxs-lookup"><span data-stu-id="d611c-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="d611c-112">Mensaje al que responde.</span><span class="sxs-lookup"><span data-stu-id="d611c-112">The message to respond to.</span></span>
  
 <span data-ttu-id="d611c-113">_wParam_ (**WParam**)</span><span class="sxs-lookup"><span data-stu-id="d611c-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="d611c-114">_lParam_ (**LParam**)</span><span class="sxs-lookup"><span data-stu-id="d611c-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="d611c-115">Argumentos pasados por Windows.</span><span class="sxs-lookup"><span data-stu-id="d611c-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d611c-116">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d611c-116">Property value/Return value</span></span>

 <span data-ttu-id="d611c-117">**True** si el mensaje se procesa, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d611c-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="d611c-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d611c-118">Example</span></span>

<span data-ttu-id="d611c-119">Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="d611c-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d611c-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="d611c-120">See also</span></span>



[<span data-ttu-id="d611c-121">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="d611c-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

