---
title: DetenerTodasMacros (acción de macro)
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 34dbfc3504744dd446a018e797ebacfb79066d96
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923354"
---
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="f00db-102">DetenerTodasMacros (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="f00db-102">StopAllMacros macro action</span></span>


<span data-ttu-id="f00db-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f00db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f00db-104">Puede usar la acción **DetenerTodasMacros** para detener todas las macros actualmente en ejecución.</span><span class="sxs-lookup"><span data-stu-id="f00db-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="f00db-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="f00db-105">Setting</span></span>

<span data-ttu-id="f00db-106">La acción **DetenerTodasMacros** no utiliza ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="f00db-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="f00db-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f00db-107">Remarks</span></span>

<span data-ttu-id="f00db-108">Esta acción se suele utilizar cuando es necesario detener todas las macros debido a un error.</span><span class="sxs-lookup"><span data-stu-id="f00db-108">You typically use this action when an error condition makes it necessary to stop all macros.</span></span> <span data-ttu-id="f00db-109">Puede usar una expresión condicional en la fila de acción de la macro que contiene esta acción.</span><span class="sxs-lookup"><span data-stu-id="f00db-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="f00db-110">Cuando la expresión se evalúa como **True** (-1), Microsoft Access detiene todas las macros.</span><span class="sxs-lookup"><span data-stu-id="f00db-110">When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="f00db-p102">Por ejemplo, podría disponer de una macro que muestre un cuadro de mensaje como una acción más de una serie de acciones complejas, incluida la ejecución de otras macros. Si el usuario hace clic en **Cancelar** en este cuadro de mensaje, la acción **DetenerTodasMacros** permite detener todas las macros que se están ejecutando.</span><span class="sxs-lookup"><span data-stu-id="f00db-p102">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros. If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="f00db-113">Si una macro ha utilizado las acciones **Eco** o **EstablecerAdvertencias** para desactivar el eco o la presentación de mensajes del sistema, la acción **DetenerTodasMacros** volverá a activarlos automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f00db-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="f00db-114">Esta acción no está disponible en un módulo de Visual Basic para Aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="f00db-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

