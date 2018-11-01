---
title: Determinar el modo de edición
TOCTitle: Determining Edit Mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: facad27e4579a28f45d88bfd4e440e420e70d913
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867940"
---
# <a name="determining-edit-mode"></a><span data-ttu-id="cbdbe-102">Determinar el modo de edición</span><span class="sxs-lookup"><span data-stu-id="cbdbe-102">Determining Edit Mode</span></span>


<span data-ttu-id="cbdbe-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbdbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbdbe-p101">ADO mantiene un búfer de edición asociado al registro activo. La propiedad **EditMode** indica si se han realizado cambios en él o si se han creado registros nuevos. Utilice **EditMode** para determinar el estado de edición del registro activo. Puede comprobar si hay cambios pendientes si se ha interrumpido un proceso de edición y determinar si se necesita utilizar los métodos **Update** o **CancelUpdate**.</span><span class="sxs-lookup"><span data-stu-id="cbdbe-p101">ADO maintains an editing buffer associated with the current record. The **EditMode** property indicates whether changes have been made to this buffer or whether a new record has been created. Use **EditMode** to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the **Update** or **CancelUpdate** method.</span></span>

<span data-ttu-id="cbdbe-108">**EditMode** devuelve una de las constantes **EditModeEnum** incluidas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cbdbe-108">**EditMode** returns one of the **EditModeEnum** constants, which are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cbdbe-109">Constante</span><span class="sxs-lookup"><span data-stu-id="cbdbe-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="cbdbe-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbdbe-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbdbe-111"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="cbdbe-111"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="cbdbe-112">Indica que no se está realizando ninguna operación de edición.</span><span class="sxs-lookup"><span data-stu-id="cbdbe-112">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbdbe-113"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="cbdbe-113"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="cbdbe-114">Indica que los datos del registro actual se han modificado, pero no se han guardado.</span><span class="sxs-lookup"><span data-stu-id="cbdbe-114">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbdbe-115"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="cbdbe-115"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="cbdbe-116">Indica que se ha llamado al método <strong>AddNew</strong> y que el registro activo en el búfer de copia es un nuevo registro que no se ha guardado en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cbdbe-116">Indicates that the <strong>AddNew</strong> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbdbe-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="cbdbe-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="cbdbe-118">Indica que se ha eliminado el registro actual.</span><span class="sxs-lookup"><span data-stu-id="cbdbe-118">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cbdbe-p102">**EditMode** sólo puede devolver un valor válido si hay un registro activo. **EditMode** devolverá un error si **BOF** o **EOF** son **True** o si se ha eliminado el registro activo.</span><span class="sxs-lookup"><span data-stu-id="cbdbe-p102">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if **BOF** or **EOF** is **True** or if the current record has been deleted.</span></span>

