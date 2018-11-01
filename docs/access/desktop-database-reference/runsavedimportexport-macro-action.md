---
title: EjecutarImportaciónExportaciónGuardada (acción de macro)
TOCTitle: RunSavedImportExport Macro Action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 48e808fa27e468dd7cb651cb5784627d5064fea0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870936"
---
# <a name="runsavedimportexport-macro-action"></a>EjecutarImportaciónExportaciónGuardada (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **EjecutarImportaciónExportaciónGuardada** para ejecutar una especificación de importación o exportación guardada que se creó mediante el Asistente para importación o el Asistente para exportación.


> [!NOTE]
> <P>[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</P>



## <a name="setting"></a>Configuración

La acción **EjecutarImportaciónExportaciónGuardada** tiene el siguiente argumento.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nombre de importación guardada o Nombre de exportación guardada</strong></p></td>
<td><p>Seleccione el nombre de una especificación de importación o exportación guardada en la lista desplegable.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

  - Esta acción de macro tiene el mismo efecto que llevar a cabo el siguiente procedimiento en Access:
    
    1.  En la pestaña **Datos externos**, haga clic en **Importaciones guardadas** o en **Exportaciones guardadas**.
    
    2.  En el cuadro de diálogo **Administrar tareas de datos**, en la pestaña **Importaciones guardadas** o **Exportaciones guardadas** (según la elección realizada en el paso anterior), haga clic en la especificación que desea ejecutar.
    
    3.  Haga clic en **Ejecutar**.

  - Antes de ejecutar la acción **EjecutarImportaciónExportaciónGuardada**, asegúrese de que existen tanto el archivo de origen como el de destino, que los datos de origen están preparados para la importación y que la operación no sobrescribirá accidentalmente ningún dato en el archivo de destino.

  - La sección **Vea también** incluye vínculos a más información sobre cómo guardar y ejecutar las especificaciones de importación y exportación.

  - Si el guardado importa o exportar especificación que elija para el argumento de **Nombre de exportación guardada** se elimina después de crearse la macro, Access muestra el siguiente mensaje de error cuando se ejecuta la macro: does de la especificación con el índice especificado de ** no existe. Especifique un índice diferente. ' *** especificación nombre ***'.**

