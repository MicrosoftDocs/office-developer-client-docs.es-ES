---
title: BloquearPanelDeExploración (acción de macro)
TOCTitle: LockNavigationPane Macro Action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2db34ee9ea56c5fcb4c5aff6afa57c3f59d1f17c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870334"
---
# <a name="locknavigationpane-macro-action"></a><span data-ttu-id="e6cbd-102">BloquearPanelDeExploración (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="e6cbd-102">LockNavigationPane Macro Action</span></span>


<span data-ttu-id="e6cbd-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6cbd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6cbd-104">Puede usar la acción **BloquearPanelDeExploración** para impedir que los usuarios eliminen objetos de base de datos que se muestran en el Panel de navegación.</span><span class="sxs-lookup"><span data-stu-id="e6cbd-104">You can use the **LockNavigationPane** action to prevent users from deleting database objects that are displayed in the Navigation Pane.</span></span>

## <a name="setting"></a><span data-ttu-id="e6cbd-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="e6cbd-105">Setting</span></span>

<span data-ttu-id="e6cbd-106">La acción **BloquearPanelDeExploración** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="e6cbd-106">The **LockNavigationPane** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6cbd-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="e6cbd-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e6cbd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6cbd-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6cbd-109"><strong>Lock</strong></span><span class="sxs-lookup"><span data-stu-id="e6cbd-109"><strong>Lock</strong></span></span></p></td>
<td><p><span data-ttu-id="e6cbd-110">Seleccione <strong>Sí</strong> para bloquear el panel de navegación, o bien, <strong>No</strong> para desbloquearlo.</span><span class="sxs-lookup"><span data-stu-id="e6cbd-110">Select <strong>Yes</strong> to lock the Navigation Pane, or <strong>No</strong> to unlock the Navigation Pane.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e6cbd-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6cbd-111">Remarks</span></span>

<span data-ttu-id="e6cbd-112">Al bloquear el panel de navegación, se impide que se eliminen objetos de la base de datos o se corten y se peguen objetos de la base de datos en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="e6cbd-112">Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard.</span></span> <span data-ttu-id="e6cbd-113">Lo hace *no* le impida llevar a cabo cualquiera de las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="e6cbd-113">It does *not* prevent you from performing any of the following operations:</span></span>

  - <span data-ttu-id="e6cbd-114">Copiar objetos de base de datos en el Portapapeles</span><span class="sxs-lookup"><span data-stu-id="e6cbd-114">Copying database objects to the clipboard</span></span>

  - <span data-ttu-id="e6cbd-115">Pegar objetos de base de datos del Portapapeles</span><span class="sxs-lookup"><span data-stu-id="e6cbd-115">Pasting database objects from the clipboard</span></span>

  - <span data-ttu-id="e6cbd-116">Mostrar u ocultar el Panel de navegación</span><span class="sxs-lookup"><span data-stu-id="e6cbd-116">Displaying or hiding the Navigation Pane</span></span>

  - <span data-ttu-id="e6cbd-117">Seleccionar esquemas de organización diferentes en el Panel de navegación</span><span class="sxs-lookup"><span data-stu-id="e6cbd-117">Selecting different Navigation Pane organization schemes</span></span>

  - <span data-ttu-id="e6cbd-118">Mostrar u ocultar secciones del Panel de navegación</span><span class="sxs-lookup"><span data-stu-id="e6cbd-118">Showing or hiding sections of the Navigation Pane</span></span>

<span data-ttu-id="e6cbd-119">Para ejecutar la acción **BloquearPanelDeExploración** en un módulo de VBA, use el método **LockNavigationPane** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="e6cbd-119">To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.</span></span>

