---
title: DesplazarseA (acción de macro)
TOCTitle: NavigateTo Macro Action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9a6a59b6c84e9814aeb9b4709d27955f29fd9e1e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484996"
---
# <a name="navigateto-macro-action"></a>DesplazarseA (acción de macro)


**Se aplica a**: Access 2013 | Office 2013

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
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Categor?a</strong></p></td>
<td><p>Argumento obligatorio. Categoría por la que el panel de navegación debe mostrar los objetos. Haga clic en <strong>Tipo de objeto</strong>, <strong>Tablas y vistas</strong>, <strong>Fecha de modificación</strong>, <strong>Fecha de creación</strong>, o bien, <strong>Personalizada</strong> en el cuadro <strong>Categoría</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Group</strong></p></td>
<td><p>Opcional. El argumento <strong>grupo</strong> limita los objetos en la categoría que aparece en el panel de navegación. Si deja en blanco el argumento <strong>grupo</strong> , el panel de navegación muestra todos los objetos de base de datos, clasificados por los criterios especificados en el argumento <strong>categoría</strong> . En la tabla siguiente se muestran ejemplos de argumentos  <strong>Group</strong> válidos para los distintos argumentos <strong>Category</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

  - Esta acción es similar a seleccionar categorías y grupos de la barra de título del Panel de navegación.

  - Los argumentos **Grupo** válidos dependen del argumento **Categoría** que se utilice. Si especifica un argumento **Grupo** no válido, aparecerá un mensaje de error.La tabla siguiente contiene ejemplo de argumentos **Grupo** válidos para cada argumento **Categoría**.
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Argumento Categoría</p></th>
    <th><p>Ejemplo de argumentos Grupo</p></th>
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
> <P>[!NOTA] Para desplazarse al nivel superior de una categoría (por ejemplo, <STRONG>Todas las tablas</STRONG>, <STRONG>Todos los objetos de Access</STRONG> o <STRONG>Todas las fechas</STRONG>), deje el argumento Grupo en blanco. Por ejemplo, cuando el valor del argumento <STRONG>Categoría</STRONG> es <STRONG>Tipo de objeto</STRONG> y se especifica <STRONG>Todos los objetos de Access</STRONG> como argumento <STRONG>Grupo</STRONG>, se genera un error.</P>


