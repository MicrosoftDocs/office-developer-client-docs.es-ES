---
title: DesplazarseA (acción de macro)
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1c37e798e0624a5655b63a76332073e5b57c0823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288605"
---
# <a name="navigateto-macro-action"></a>DesplazarseA (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **DesplazarseA** para controlar la presentación de los objetos de la base de datos en el panel de navegación. Por ejemplo, puede cambiar la manera en que los objetos de la base de datos se organizan en categorías o puede filtrar los objetos de modo que solo se muestren determinados objetos.

## <a name="setting"></a>Configuración

La acción **DesplazarseA** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Categoría</strong></p></td>
<td><p>Argumento obligatorio. Categoría por la que el panel de navegación debe mostrar los objetos. Haga clic en <strong>Tipo de objeto</strong>, <strong>Tablas y vistas</strong>, <strong>Fecha de modificación</strong>, <strong>Fecha de creación</strong>, o bien, <strong>Personalizada</strong> en el cuadro <strong>Categoría</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Agrupar</strong></p></td>
<td><p>Opcional. El argumento <strong>Grupo</strong> limita los objetos que van a aparecer en el panel de navegación. Si deja el argumento <strong>Group</strong> en blanco, el panel de navegación muestra todos los objetos de base de datos, categorizados por los criterios especificados en el <strong>argumento Category.</strong> La siguiente tabla incluye ejemplos de argumentos <strong>Grupo</strong> válidos para los diversos argumentos <strong>Categoría</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

- Esta acción es similar a seleccionar categorías y grupos de la barra de título del panel de navegación.

- Los argumentos **Grupo** válidos dependen del argumento **Categoría** que se utilice. Si especifica un argumento **Grupo** no válido, aparecerá un mensaje de error.La tabla siguiente contiene ejemplo de argumentos **Grupo** válidos para cada argumento **Categoría**.
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p>Argumento Category</p></th>
  <th><p>Ejemplo de argumentos Group</p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p>Tipo de objeto</p></td>
  <td><p>Tablas; Formularios; Consultas; Páginas; Macros; Módulos</p></td>
  </tr>
  <tr class="even">
  <td><p>Tablas y vistas</p></td>
  <td><p>Nombres de tablas específicas de la base de datos</p></td>
  </tr>
  <tr class="odd">
  <td><p>Fecha de modificación</p></td>
  <td><p>Hoy; Ayer; Mes pasado; Con más de</p></td>
  </tr>
  <tr class="even">
  <td><p>Fecha de creación</p></td>
  <td><p>Hoy; Ayer; El mes pasado; Antiguo</p></td>
  </tr>
  <tr class="odd">
  <td><p>Categoría personalizada</p></td>
  <td><p>Nombres de grupos que creó para la categoría personalizada especificada</p></td>
  </tr>
  </tbody>
  </table>

- Para ejecutar la acción **DesplazarseA** en un módulo de VBA, use el método **NavigateTo** del objeto **DoCmd**.

> [!NOTE]
> [!NOTA] Para desplazarse al nivel superior de una categoría (por ejemplo, **Todas las tablas**, **Todos los objetos de Access** o **Todas las fechas**), deje el argumento Grupo en blanco. Por ejemplo, cuando el valor del argumento **Categoría** es **Tipo de objeto** y se especifica **Todos los objetos de Access** como argumento **Grupo**, se genera un error.


