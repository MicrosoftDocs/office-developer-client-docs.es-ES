---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- excelcursorproc (función) [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815626"
---
# <a name="excelcursorproc"></a><span data-ttu-id="d0d27-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="d0d27-104">ExcelCursorProc</span></span>

 <span data-ttu-id="d0d27-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d0d27-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d0d27-106">Cuando se muestra un cuadro de diálogo modal a través de la ventana de Microsoft Excel, el cursor es un cursor no disponible a través de la ventana de Excel.</span><span class="sxs-lookup"><span data-stu-id="d0d27-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="d0d27-107">Este capturas **WndProc** WM_SETCURSOR escriba mensajes de Windows y los cambios que se copia el cursor a una flecha normal.</span><span class="sxs-lookup"><span data-stu-id="d0d27-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="d0d27-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0d27-108">Parameters</span></span>

 <span data-ttu-id="d0d27-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="d0d27-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="d0d27-110">Contiene el identificador de Windows de HWND del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d0d27-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="d0d27-111">_mensaje_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="d0d27-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="d0d27-112">El mensaje para responder a.</span><span class="sxs-lookup"><span data-stu-id="d0d27-112">The message to respond to.</span></span>
  
 <span data-ttu-id="d0d27-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="d0d27-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="d0d27-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="d0d27-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="d0d27-115">Argumentos que se pasan por parte de Windows.</span><span class="sxs-lookup"><span data-stu-id="d0d27-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d0d27-116">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0d27-116">Property value/Return value</span></span>

<span data-ttu-id="d0d27-117">LRESULT: 0 si se ha controlado el mensaje, en caso contrario, el resultado devuelto por el valor predeterminado **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="d0d27-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="d0d27-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0d27-118">Example</span></span>

<span data-ttu-id="d0d27-119">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="d0d27-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d0d27-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0d27-120">See also</span></span>



[<span data-ttu-id="d0d27-121">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="d0d27-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

