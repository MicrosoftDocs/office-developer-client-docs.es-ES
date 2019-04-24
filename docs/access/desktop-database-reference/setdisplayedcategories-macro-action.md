---
title: DefinirCategoríasMostradas (acción de macro)
TOCTitle: SetDisplayedCategories macro action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f08b9a8980fc6f08a9f91366d38f65e4365a037e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314629"
---
# <a name="setdisplayedcategories-macro-action"></a><span data-ttu-id="de677-102">DefinirCategoríasMostradas (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="de677-102">SetDisplayedCategories macro action</span></span>


<span data-ttu-id="de677-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de677-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de677-p101">Puede usar la acción **DefinirCategoríasMostradas** para especificar las categorías que se van a mostrar bajo **Desplazarse a la categoría** en la barra de título del panel de navegación. Por ejemplo, si desea impedir que los usuarios puedan cambiar el panel de navegación de modo que muestre los objetos ordenados por **Fecha de creación**, puede usar esta acción para ocultar esa opción en la lista desplegable de la barra de título.</span><span class="sxs-lookup"><span data-stu-id="de677-p101">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane. For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span></span>

## <a name="setting"></a><span data-ttu-id="de677-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="de677-106">Setting</span></span>

<span data-ttu-id="de677-107">La acción **DefinirCategoríasMostradas** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="de677-107">The **SetDisplayedCategories** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de677-108">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="de677-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="de677-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="de677-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de677-110"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="de677-110"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="de677-111">Seleccione <strong>Sí</strong> para que se muestren las categorías.</span><span class="sxs-lookup"><span data-stu-id="de677-111">Select <strong>Yes</strong> to show the category or categories.</span></span> <span data-ttu-id="de677-112">Seleccione <strong>No</strong> para ocultarlas.</span><span class="sxs-lookup"><span data-stu-id="de677-112">Select <strong>No</strong> to hide them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de677-113"><strong>Categoría</strong></span><span class="sxs-lookup"><span data-stu-id="de677-113"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="de677-114">Especifique o seleccione el nombre de la categoría que desee mostrar u ocultar.</span><span class="sxs-lookup"><span data-stu-id="de677-114">Enter or select the name of the category you want to show or hide.</span></span> <span data-ttu-id="de677-115">Deje este argumento en blanco para mostrar u ocultar todas las categorías.</span><span class="sxs-lookup"><span data-stu-id="de677-115">Leave blank to show or hide all categories.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="de677-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de677-116">Remarks</span></span>

  - <span data-ttu-id="de677-p104">El título en la barra de título del panel de navegación indica, si procede, el filtro actualmente activo. Haga clic en cualquier punto de la barra para mostrar la lista desplegable. Los elementos controlados por esta acción de macro aparecen bajo **Desplazarse a la categoría**.</span><span class="sxs-lookup"><span data-stu-id="de677-p104">The caption in the title bar of the Navigation pane indicates which filter, if any, is currently active. Click anywhere in the bar to display the drop-down list. The items that this macro action controls are listed under **Navigate to Category**.</span></span>

  - <span data-ttu-id="de677-p105">Esta acción sólo activa o desactiva la presentación de las categorías especificadas; no cambia la presentación del panel de navegación. Por ejemplo, si se muestran objetos ordenados por **Fecha de creación** y se usa la acción **DefinirCategoríasMostradas** para deshabilitar la opción **Fecha de creación**, Access no cambia el panel de navegación a otra categoría.</span><span class="sxs-lookup"><span data-stu-id="de677-p105">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display. For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span></span>

  - <span data-ttu-id="de677-122">Para ejecutar la acción **DefinirCategoríasMostradas** en un módulo de VBA, use el método **SetDisplayedCategories** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="de677-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span></span>

