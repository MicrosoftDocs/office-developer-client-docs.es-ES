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
# <a name="dialogmsgproc"></a><span data-ttu-id="2192e-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="2192e-104">DIALOGMsgProc</span></span>

<span data-ttu-id="2192e-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2192e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2192e-106">Este procedimiento está asociada con el cuadro de diálogo nativo de Windows muestra que [fShowDialog](fshowdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2192e-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="2192e-107">Proporciona las rutinas de servicio llamadas por Windows para los eventos (mensajes) que se producen cuando el usuario opera uno de los botones del cuadro de diálogo, los campos de entrada o controles.</span><span class="sxs-lookup"><span data-stu-id="2192e-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="2192e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2192e-108">Parameters</span></span>

 <span data-ttu-id="2192e-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="2192e-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="2192e-110">Contiene el identificador de Windows de HWND del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2192e-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="2192e-111">_mensaje_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="2192e-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="2192e-112">El mensaje para responder a.</span><span class="sxs-lookup"><span data-stu-id="2192e-112">The message to respond to.</span></span>
  
 <span data-ttu-id="2192e-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="2192e-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="2192e-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="2192e-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="2192e-115">Argumentos que se pasan por parte de Windows.</span><span class="sxs-lookup"><span data-stu-id="2192e-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2192e-116">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2192e-116">Property value/Return value</span></span>

 <span data-ttu-id="2192e-117">**TRUE** si el mensaje procesado, **FALSE** si no.</span><span class="sxs-lookup"><span data-stu-id="2192e-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="2192e-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2192e-118">Example</span></span>

<span data-ttu-id="2192e-119">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="2192e-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2192e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2192e-120">See also</span></span>



[<span data-ttu-id="2192e-121">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="2192e-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

