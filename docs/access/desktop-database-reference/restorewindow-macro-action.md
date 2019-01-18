---
title: RestaurarVentana (acción de macro)
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 35637781035b7a449ba574cf5f6c84f2cb5223db
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718836"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="bb2a2-102">RestaurarVentana (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="bb2a2-102">RestoreWindow macro action</span></span>

<span data-ttu-id="bb2a2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb2a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb2a2-104">Puede usar la acción **RestaurarVentana** para restaurar el tamaño que tenía anteriormente una ventana maximizada o minimizada.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>

> [!NOTE]
> <span data-ttu-id="bb2a2-p101">[!NOTA] Esta acción no puede aplicarse a las ventanas de código en el Editor de Visual Basic. Para obtener información sobre cómo afectar a las ventanas de código, vea el tema de la propiedad **WindowState**.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="bb2a2-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="bb2a2-107">Setting</span></span>

<span data-ttu-id="bb2a2-108">La acción **RestaurarVentana** no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb2a2-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb2a2-109">Remarks</span></span>

<span data-ttu-id="bb2a2-p102">Esta acción funciona en el objeto seleccionado. Si se ha minimizado un objeto, primero puede seleccionarlo con la acción **SeleccionarObjeto** y, a continuación, restaurar su tamaño anterior mediante la acción **RestaurarVentana**.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-p102">This action works on the selected object. If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="bb2a2-112">Se puede usar la acción **MoverYCambiarTamañoDeVentana** para mover o cambiar el tamaño de una ventana restaurada.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="bb2a2-113">La acción **RestaurarVentana** tiene el mismo efecto que hacer clic en el botón **Restaurar** situado en la esquina superior derecha de la ventana o hacer clic en el comando **Restaurar** del menú **Control** de la ventana.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="bb2a2-114">Para ejecutar la acción **RestaurarVentana** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Restore** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

