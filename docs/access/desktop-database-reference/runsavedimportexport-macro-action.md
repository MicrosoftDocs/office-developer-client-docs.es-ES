---
title: EjecutarImportaciónExportaciónGuardada (acción de macro)
TOCTitle: RunSavedImportExport macro action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: adcc8a2a9462509f4b37d2dbdaf824387ae52a26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309180"
---
# <a name="runsavedimportexport-macro-action"></a><span data-ttu-id="d46ed-102">EjecutarImportaciónExportaciónGuardada (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="d46ed-102">RunSavedImportExport macro action</span></span>

<span data-ttu-id="d46ed-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d46ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d46ed-104">Puede usar la acción **EjecutarImportaciónExportaciónGuardada** para ejecutar una especificación de importación o exportación guardada que se creó mediante el Asistente para importación o el Asistente para exportación.</span><span class="sxs-lookup"><span data-stu-id="d46ed-104">You can use the **RunSavedImportExport** action to run a saved import or export specification that you created by using the Import Wizard or the Export Wizard.</span></span>

> [!NOTE]
> <span data-ttu-id="d46ed-105">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="d46ed-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="d46ed-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="d46ed-106">Setting</span></span>

<span data-ttu-id="d46ed-107">La acción **EjecutarImportaciónExportaciónGuardada** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="d46ed-107">The **RunSavedImportExport** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d46ed-108">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="d46ed-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d46ed-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d46ed-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d46ed-110"><strong>Nombre de importación guardada o Nombre de exportación guardada</strong></span><span class="sxs-lookup"><span data-stu-id="d46ed-110"><strong>Saved Import Export Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ed-111">Seleccione el nombre de una especificación de importación o exportación guardada en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="d46ed-111">Select the name of a saved import or export specification from the drop-down list.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d46ed-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d46ed-112">Remarks</span></span>

- <span data-ttu-id="d46ed-113">Esta acción de macro tiene el mismo efecto que llevar a cabo el siguiente procedimiento en Access:</span><span class="sxs-lookup"><span data-stu-id="d46ed-113">This macro action has the same effect as performing the following procedure in Access:</span></span>
    
  1.  <span data-ttu-id="d46ed-114">En la pestaña **Datos externos**, haga clic en **Importaciones guardadas** o en **Exportaciones guardadas**.</span><span class="sxs-lookup"><span data-stu-id="d46ed-114">On the **External Data** tab, click either **Saved Imports** or **Saved Exports**.</span></span>
    
  2.  <span data-ttu-id="d46ed-115">En el cuadro de diálogo **Administrar tareas de datos**, en la pestaña **Importaciones guardadas** o **Exportaciones guardadas** (según la elección realizada en el paso anterior), haga clic en la especificación que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="d46ed-115">In the **Manage Data Tasks** dialog box, on the **Saved Imports** or **Saved Exports** tab (depending on your choice in the preceding step), click the specification that you want to run.</span></span>
    
  3.  <span data-ttu-id="d46ed-116">Haga clic en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="d46ed-116">Click **Run**.</span></span>

- <span data-ttu-id="d46ed-117">Antes de ejecutar la acción **EjecutarImportaciónExportaciónGuardada**, asegúrese de que existen tanto el archivo de origen como el de destino, que los datos de origen están preparados para la importación y que la operación no sobrescribirá accidentalmente ningún dato en el archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d46ed-117">Before running the **RunSavedImportExport** action, make sure that the source and destination files exist, the source data is ready for importing, and that the operation will not accidentally overwrite any data in your destination file.</span></span>

- <span data-ttu-id="d46ed-118">La sección **Vea también** incluye vínculos a más información sobre cómo guardar y ejecutar las especificaciones de importación y exportación.</span><span class="sxs-lookup"><span data-stu-id="d46ed-118">Find links to more information about saving and running import and export specifications in the **See Also** section.</span></span>

- <span data-ttu-id="d46ed-119">Si la especificación de importación o exportación guardada elegida para el argumento **nombre de importación y exportación guardada** se elimina una vez creada la macro, Access muestra el siguiente mensaje de error cuando se ejecuta la macro: **la especificación con el índice especificado no existir. Especifique un índice diferente. ' \* \* \* \* \* nombre de especificación \* \* \* \* \* '.**</span><span class="sxs-lookup"><span data-stu-id="d46ed-119">If the saved import or export specification you choose for the **Saved Import Export Name** argument is deleted after the macro is created, Access displays the following error message when the macro is run: **The specification with the specified index does not exist. Specify a different index. '\*\*\*\*\*specification name\*\*\*\*\*'.**</span></span>

