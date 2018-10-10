---
title: AplicarFiltro (acción de macro)
TOCTitle: ApplyFilter Macro Action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fc90d6cc2cdb3f4bbee4faeb48e12555c14fa9a1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484675"
---
# <a name="applyfilter-macro-action"></a>AplicarFiltro (acción de macro)

**Se aplica a**: Access 2013 | Office 2013

Puede usar la acción **AplicarFiltro** para aplicar un filtro, una consulta o una cláusula WHERE de SQL a una tabla, un formulario o un informe para restringir u ordenar los registros en la tabla, o los registros de la tabla subyacente o la consulta del formulario o informe. Para los informes, puede usar esta acción solo en una macro especificada por la propiedad del evento **OnOpen** del informe.

> [!NOTE]
> [!NOTA] Puede usar esta acción para aplicar una cláusula WHERE de SQL cuando aplique un filtro de servidor. Un filtro de servidor no se puede aplicar a una fuente de registros de un procedimiento almacenado.

## <a name="setting"></a>Configuración

La acción **AplicarFiltro** tiene los siguientes argumentos.

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
<td><p>Filter Name</p></td>
<td><p>El nombre de un filtro o una consulta que restringe u ordena los registros de una tabla, un formulario o un informe. Puede escribir el nombre de una consulta existente o un filtro que se guardó como una consulta en el cuadro <strong>Nombre del filtro</strong> de la sección <strong>Argumentos de acciones</strong> del panel <strong>Generador de macros</strong>.  </p>

> [!NOTE]
> Cuando utiliza esta acción para aplicar un filtro de servidor, el argumento Filter Name debe estar vacío.


<p></p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>Una cláusula WHERE válida de SQL (sin la palabra WHERE) o una expresión que restringe los registros de la tabla, el formulario o el informe.</p>
<p><b>Nota</b>: expresión del argumento en una condición Where, el lado izquierdo de la expresión contiene normalmente un nombre de campo de la tabla o consulta subyacente del formulario o informe. El lado derecho de la expresión contiene normalmente los criterios que desea aplicar a este campo para restringir u ordenar los registros. Por ejemplo, los criterios pueden ser el nombre de un control de otro formulario que contiene el valor que desea que los registros en el primer formulario para que coincida con. El nombre del control debe ser completo, por ejemplo:</p>
<p><strong>Formularios</strong>! <em>formname</em>! <em>controlname</em> Los nombres de campo deben estar encerrados entre comillas dobles y los literales de cadena deben estar encerrados entre comillas simples. La longitud máxima del argumento Condición Where es de 255 caracteres. Si necesita escribir una cláusula WHERE de SQL más larga, utilice el método <strong>ApplyFilter</strong> del objeto <strong>DoCmd</strong> en un de Visual Basic para aplicaciones (VBA). Puede especificar instrucciones de cláusula WHERE de SQL de hasta 32.768 caracteres en VBA.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Puede usar el argumento nombre del filtro si ya ha definido un filtro que proporciona los datos adecuados. Puede usar el argumento Condición Where para especificar directamente los criterios de restricción. Si usa ambos argumentos, Microsoft Office Access 2007 aplica la cláusula WHERE a los resultados del filtro. Debe usar uno o ambos argumentos.

## <a name="remarks"></a>Comentarios

Puede aplicar un filtro o una consulta a un formulario en la vista Formulario o la vista Hoja de datos.

El filtro y la condición WHERE que aplica se convierten en la configuración de la propiedad **Filter** o **ServerFilter** del formulario o el informe.

Para las tablas y los formularios, esta acción es similar a hacer clic en **Aplicar filtro u orden** o **Aplicar filtro de servidor** en el menú **Registros**. El comando de menú aplica el filtro creado más recientemente a la tabla o el formulario, mientras que la acción **AplicarFiltro** aplica un filtro o una consulta especificada.

En una base de datos de Access, si va a **Filtro** en el menú **Registros** y hace clic en **Filtro u orden avanzado** después de ejecutar la acción **AplicarFiltro**, la ventana Filtro u orden avanzado muestra los criterios de filtro que seleccionó con esta acción.

Para quitar un filtro y mostrar todos los registros para una tabla o un formulario en una Office Access 2007 base de datos, puede utilizar la acción **MostrarTodosRegistros** o el comando **Quitar filtro u orden** en el menú **Registros**. Para quitar un filtro en un proyecto de Access (.adp), puede volver a la ventana Filtro de servidor por formulario y quitar todos los criterios de filtros, y hacer clic en **Aplicar filtro de servidor** en el menú **Registros** de la barra de herramientas, o establecer la propiedad **ServerFilterByForm** a **False** (0).

Cuando guarda una tabla o un formulario, Access guarda cualquier filtro definido actualmente en ese objeto, pero no aplica el filtro automáticamente la próxima vez que se abre el objeto (aunque aplicará automáticamente cualquier orden que usted aplicó al objeto antes de guardarlo). Si desea aplicar un filtro automáticamente cuando se abre un formulario por primera vez, especifique una macro que contenga la acción **AplicarFiltro** o un procedimiento de evento que contenga el método **ApplyFilter** del objeto **DoCmd** como la configuración de la propiedad de evento **OnOpen** del formulario. También puede aplicar un filtro al utilizar la acción **AbrirFormulario** o **AbrirInforme**, o sus correspondientes métodos. Para aplicar un filtro automáticamente cuando se abre una tabla por primera vez, puede abrir la tabla con una macro que contenga la acción **AbrirTabla**, seguida inmediatamente por la acción **AplicarFiltro**.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar la acción ApplyFilter para filtrar el formulario frmFoods cuando se abre.

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```



