---
title: MaximizarVentana (acción de macro)
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 262e6781b61018cec3d52dbb930f380d3ff5bd85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289752"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="1680e-102">MaximizarVentana (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="1680e-102">MaximizeWindow macro action</span></span>

<span data-ttu-id="1680e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1680e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1680e-104">Si Access está configurado para usar ventanas superpuestas en lugar de documentos con fichas, puede usar la acción **MaximizarVentana** para ampliar la ventana activa de modo que llene la ventana de Access.</span><span class="sxs-lookup"><span data-stu-id="1680e-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="1680e-105">Esta acción permite ver el máximo posible del objeto en la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="1680e-105">This action will allow you to see as much of the object in the active window as possible.</span></span>

> [!NOTE]
> <span data-ttu-id="1680e-p102">[!NOTA] Esta acción no puede aplicarse a las ventanas de código en el Editor de Visual Basic. Para obtener información sobre cómo afectar a las ventanas de código, vea el tema de la propiedad **WindowState**.</span><span class="sxs-lookup"><span data-stu-id="1680e-p102">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="1680e-108">Setting</span><span class="sxs-lookup"><span data-stu-id="1680e-108">Setting</span></span>

<span data-ttu-id="1680e-109">La acción **MaximizarVentana** no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="1680e-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="1680e-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1680e-110">Remarks</span></span>

<span data-ttu-id="1680e-111">Esta acción tiene el mismo efecto que hacer clic en el botón **Maximizar** situado en la esquina superior derecha de la ventana o hacer clic en **Maximizar** en el menú **Control** de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1680e-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="1680e-112">Se puede utilizar la acción **RestaurarVentana** para restaurar el tamaño que tenía anteriormente una ventana maximizada.</span><span class="sxs-lookup"><span data-stu-id="1680e-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

> [!TIP]
> - <span data-ttu-id="1680e-113">Si la ventana que desea maximizar no es la ventana activa, puede que sea necesario utilizar la acción **SeleccionarObjeto**.</span><span class="sxs-lookup"><span data-stu-id="1680e-113">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>
> - <span data-ttu-id="1680e-p103">Si se maximiza una ventana en Access, las demás ventanas también se maximizarán al abrirlas o al cambiar a ellas. Sin embargo, los formularios emergentes no se maximizarán. Si desea que un formulario mantenga su tamaño cuando maximice otras ventanas, establezca el valor de la propiedad **Emergente** en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="1680e-p103">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them. However, pop-up forms aren't maximized. If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="1680e-117">Para ejecutar la acción **MaximizarVentana** desde un módulo de Visual Basic para Aplicaciones, use el método **Maximize** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="1680e-117">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

