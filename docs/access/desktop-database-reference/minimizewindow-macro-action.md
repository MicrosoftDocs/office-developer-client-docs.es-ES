---
title: MinimizarVentana (acción de macro)
TOCTitle: MinimizeWindow macro action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 50716a32d0fa3837f87d9d2c5ecde0b59696480d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920371"
---
# <a name="minimizewindow-macro-action"></a><span data-ttu-id="cb51d-102">MinimizarVentana (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="cb51d-102">MinimizeWindow macro action</span></span>


<span data-ttu-id="cb51d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb51d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb51d-104">Si Access está configurado para utilizar ventanas superpuestas en lugar de documentos con fichas, puede utilizar la acción **Minimizarventana** para reducir la ventana activa a una barra de título pequeña en la parte inferior de la ventana de Access.</span><span class="sxs-lookup"><span data-stu-id="cb51d-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MinimizeWindow** action to reduce the active window to a small title bar at the bottom of the Access window.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cb51d-p101">[!NOTA] Esta acción no puede aplicarse a las ventanas de código en el Editor de Visual Basic. Para obtener información sobre cómo afectar a las ventanas de código, vea el tema de la propiedad <STRONG>WindowState</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="cb51d-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="cb51d-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="cb51d-107">Setting</span></span>

<span data-ttu-id="cb51d-108">La acción **MinimizarVentana** no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="cb51d-108">The **MinimizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb51d-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb51d-109">Remarks</span></span>

<span data-ttu-id="cb51d-p102">Puede usar esta acción para quitar una ventana de la pantalla sin cerrar el objeto. También puede utilizarla para abrir un objeto sin mostrar su ventana. Para mostrar el objeto, utilice la acción **SeleccionarObjeto** con la acción **MaximizarVentana** o **RestaurarVentana**. La acción **RestaurarVentana** restaura el tamaño anterior de una ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="cb51d-p102">You can use this action to remove a window from the screen while leaving the object open. You can also use this action to open an object without displaying its window. To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action. The **RestoreWindow** action restores a minimized window to its previous size.</span></span>

<span data-ttu-id="cb51d-114">La acción **MinimizarVentana** tiene el mismo efecto que hacer clic en el botón **Minimizar** situado en la esquina superior derecha de la ventana o hacer clic en **Minimizar** en el menú **Control** de la ventana.</span><span class="sxs-lookup"><span data-stu-id="cb51d-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span></span>

<span data-ttu-id="cb51d-115">**Sugerencias**</span><span class="sxs-lookup"><span data-stu-id="cb51d-115">**Tips**</span></span>

  - <span data-ttu-id="cb51d-116">Si la ventana que desea minimizar no es la ventana activa, puede que primero sea necesario utilizar la acción **SeleccionarObjeto**.</span><span class="sxs-lookup"><span data-stu-id="cb51d-116">You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.</span></span>

  - <span data-ttu-id="cb51d-p103">Para ocultar el panel de navegación, utilice la acción **SeleccionarObjeto** con el valor del argumento En panel de navegación establecido en **Sí** y, a continuación, utilice la acción **MinimizarVentana**. El objeto que seleccione con la acción **SeleccionarObjeto** puede ser cualquiera de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cb51d-p103">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action. The object you select in the **SelectObject** action can be any object in the database.</span></span>

  - <span data-ttu-id="cb51d-p104">Puede ocultar la ventana activa, haciendo clic en **Administrar esta ventana** en el menú **Ver** y, a continuación, en **Ocultar**. En lugar de reducirse a un icono, la ventana deja de estar visible. Utilice el comando **Mostrar** del mismo menú para que vuelva a aparecer la ventana. Puede usar la acción **EjecutarComandoDeMenú** para ejecutar cualquiera de estos comandos desde una macro.</span><span class="sxs-lookup"><span data-stu-id="cb51d-p104">You can hide the active window by clicking **Manage This Window** on the **View** menu, and then clicking **Hide**. Instead of being reduced to an icon, the window becomes invisible. Use the **Unhide** command on the same menu to make the window reappear. You can use the **RunMenuCommand** action to carry out either of these commands from a macro.</span></span>

  - <span data-ttu-id="cb51d-123">También puede utilizar la acción **EstablecerValor** para establecer el valor de la propiedad **Visible** de un formulario de manera que se oculte o se muestre su ventana.</span><span class="sxs-lookup"><span data-stu-id="cb51d-123">You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.</span></span>

<span data-ttu-id="cb51d-124">Para ejecutar la acción **MinimizarVentana** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Minimize** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="cb51d-124">To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.</span></span>

