---
title: Mostrar cuadros de diálogo desde dentro de una DLL o XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL [excel 2007], mostrar cuadros de diálogo de cuadros de diálogo [Excel 2007], mostrar desde una DLL o XLL, archivos DLL [Excel 2007], mostrar cuadros de diálogo de
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815536"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="82f25-104">Mostrar cuadros de diálogo desde dentro de una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="82f25-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="82f25-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="82f25-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="82f25-106">Para mostrar un cuadro de diálogo de Win32, por ejemplo, mediante la función de Windows SDK **DialogBox**, primero debe obtener la instancia completa de 32 bits y los identificadores de ventana principal de Excel.</span><span class="sxs-lookup"><span data-stu-id="82f25-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="82f25-107">Para obtener más información, vea [acceso instancia de Excel y los identificadores de ventana principal](how-to-access-excel-instance-and-main-window-handles.md).</span><span class="sxs-lookup"><span data-stu-id="82f25-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="82f25-108">Suponiendo que el proyecto contiene el recurso de cuadro de diálogo, debe seguir varios pasos para establecer la rutina de tratamiento de mensajes en los el cuadro de diálogo mostrado recientemente y para restaurar el mensaje Excel rutina de control cuando se cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="82f25-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="82f25-109">El comando de ejemplo [fShowDialog](fshowdialog.md) en el proyecto genérico, se muestra el uso de las funciones de Windows para hacer esto correctamente.</span><span class="sxs-lookup"><span data-stu-id="82f25-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="82f25-110">También puede mostrar cuadros de diálogo mediante la API de C sin tener que usar funciones del SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="82f25-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="82f25-111">Sin embargo, las capacidades de cuadro de diálogo de la API de C son muy limitadas en comparación con los de Windows, Visual Basic para aplicaciones (VBA) o Microsoft Foundation Classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="82f25-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="82f25-112">(Por ejemplo, cuadros de diálogo de la API de C son siempre modales).</span><span class="sxs-lookup"><span data-stu-id="82f25-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82f25-113">Ver también</span><span class="sxs-lookup"><span data-stu-id="82f25-113">See also</span></span>



[<span data-ttu-id="82f25-114">Creación de XLL</span><span class="sxs-lookup"><span data-stu-id="82f25-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="82f25-115">Desarrollo de DLL</span><span class="sxs-lookup"><span data-stu-id="82f25-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="82f25-116">Obtener acceso a la instancia de Excel y los identificadores de ventana principal</span><span class="sxs-lookup"><span data-stu-id="82f25-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="82f25-117">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="82f25-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

