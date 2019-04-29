---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- función excelcursorproc [Excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432495"
---
# <a name="excelcursorproc"></a><span data-ttu-id="08625-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="08625-104">ExcelCursorProc</span></span>

 <span data-ttu-id="08625-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="08625-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="08625-106">Cuando se muestra un cuadro de diálogo modal sobre la ventana de Microsoft Excel, el cursor es un cursor de ocupado sobre la ventana de Excel.</span><span class="sxs-lookup"><span data-stu-id="08625-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="08625-107">Este **WndProc** revienta WM_SETCURSOR escribe mensajes de Windows y vuelve a cambiar el cursor a una flecha normal.</span><span class="sxs-lookup"><span data-stu-id="08625-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="08625-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="08625-108">Parameters</span></span>

 <span data-ttu-id="08625-109">_hWndDlg_ (**HWnd**)</span><span class="sxs-lookup"><span data-stu-id="08625-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="08625-110">Contiene el identificador de ventana de HWND del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="08625-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="08625-111">_mensaje de error_ (**Uint**)</span><span class="sxs-lookup"><span data-stu-id="08625-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="08625-112">Mensaje al que responde.</span><span class="sxs-lookup"><span data-stu-id="08625-112">The message to respond to.</span></span>
  
 <span data-ttu-id="08625-113">_wParam_ (**WParam**)</span><span class="sxs-lookup"><span data-stu-id="08625-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="08625-114">_lParam_ (**LParam**)</span><span class="sxs-lookup"><span data-stu-id="08625-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="08625-115">Argumentos pasados por Windows.</span><span class="sxs-lookup"><span data-stu-id="08625-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="08625-116">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08625-116">Property value/Return value</span></span>

<span data-ttu-id="08625-117">LRESULT: 0 si se controló el mensaje; de lo contrario, el resultado devuelto por el **WndProc**predeterminado.</span><span class="sxs-lookup"><span data-stu-id="08625-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="08625-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08625-118">Example</span></span>

<span data-ttu-id="08625-119">Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="08625-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08625-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="08625-120">See also</span></span>



[<span data-ttu-id="08625-121">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="08625-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

