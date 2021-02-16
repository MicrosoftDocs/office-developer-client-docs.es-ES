---
title: Mostrar cuadros de diálogo desde dentro de un DLL o XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlls [excel 2007], mostrar cuadros de diálogo de,cuadros de diálogo [Excel 2007], mostrar desde un DLL o XLL,DLL [Excel 2007], mostrar cuadros de diálogo de
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417871"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="a81b4-104">Mostrar cuadros de diálogo desde dentro de un DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="a81b4-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="a81b4-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a81b4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a81b4-106">Para mostrar un cuadro de diálogo de Win32 con, por ejemplo, la función **DialogBox** de Windows SDK, primero debe obtener la instancia completa de 32 bits y los controladores de ventana principal para Excel.</span><span class="sxs-lookup"><span data-stu-id="a81b4-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="a81b4-107">Para obtener más información, vea [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span><span class="sxs-lookup"><span data-stu-id="a81b4-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="a81b4-108">Suponiendo que el proyecto contiene el recurso de cuadro de diálogo, debe realizar varios pasos para establecer la rutina de control de mensajes en la del cuadro de diálogo que se acaba de mostrar y para restaurar la rutina de control de mensajes de Excel cuando se cierre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a81b4-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="a81b4-109">El comando [de ejemplo fShowDialog](fshowdialog.md) en el proyecto genérico muestra el uso de las funciones de Windows para hacerlo correctamente.</span><span class="sxs-lookup"><span data-stu-id="a81b4-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="a81b4-110">También puedes mostrar cuadros de diálogo con la API de C sin tener que usar funciones de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a81b4-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="a81b4-111">Sin embargo, las capacidades de cuadro de diálogo de la API de C son muy limitadas en comparación con las de Windows, Visual Basic para Aplicaciones (VBA) o Microsoft Foundation Classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="a81b4-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="a81b4-112">(Por ejemplo, los cuadros de diálogo de la API de C siempre son modales).</span><span class="sxs-lookup"><span data-stu-id="a81b4-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a81b4-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="a81b4-113">See also</span></span>



[<span data-ttu-id="a81b4-114">Crear XLL</span><span class="sxs-lookup"><span data-stu-id="a81b4-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="a81b4-115">Desarrollar DLL</span><span class="sxs-lookup"><span data-stu-id="a81b4-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="a81b4-116">Obtener acceso a la instancia de Excel y los controladores de la ventana principal</span><span class="sxs-lookup"><span data-stu-id="a81b4-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="a81b4-117">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="a81b4-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

