---
title: AbrirInforme (acción de macro)
TOCTitle: OpenReport macro action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cff57a185d226328792bef79072dfc46c6134f98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288353"
---
# <a name="openreport-macro-action"></a>AbrirInforme (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **AbrirInforme** para abrir un informe en la vista Diseño o Vista preliminar, o bien, para enviar el informe directamente a la impresora. También puede restringir los registros que se imprimen en el informe.

## <a name="setting"></a>Configuración

La acción **AbrirInforme** tiene los siguientes argumentos.

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
<td><p>Nombre del informe</p></td>
<td><p>Nombre del informe que se va a abrir. El cuadro <strong>Nombre del informe</strong> en la sección <strong>Argumentos de acción</strong> del panel <strong>Generador de macros</strong> muestra todos los informes de la base de datos activa. Este es un argumento obligatorio. Si ejecuta una macro que contenga la acción OpenReport en una base de datos de biblioteca, Microsoft Access primero buscará el informe con este nombre en la base de datos de biblioteca y después en la base de datos actual.  </p></td>
</tr>
<tr class="even">
<td><p>Ver</p></td>
<td><p>Vista en la que se va a abrir el informe. Haga clic en <strong>Imprimir</strong> (para imprimir el informe de inmediato), <strong>Diseño</strong> o <strong>Vista preliminar</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Imprimir</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p>Nombre del filtro</p></td>
<td><p>Filtro que restringe los registros del informe. Puede escribir el nombre de una consulta existente o de un filtro que se guardó como consulta. No obstante, la consulta debe incluir todos los campos del informe que está abriendo o tener su propiedad <strong>SalidaTodosLosCampos</strong> establecida en <strong>Sí</strong>.  </p></td>
</tr>
<tr class="even">
<td><p>Condición WHERE</p></td>
<td><p>Una cláusula SQL WHERE válida (sin la palabra WHERE) o una expresión que usa Access para seleccionar registros de la tabla o consulta subyacente al informe. Si selecciona un filtro con el argumento Nombre de filtro, Access aplica esta cláusula WHERE a los resultados del filtro. Para abrir un informe y restringir sus registros a los especificados por el valor de un control en un formulario, use la siguiente expresión:<br />
<strong>[</strong><em>fieldname</em><strong>] = Forms! [</strong><em>formname</em><strong>]! [</strong><em>controlname en el formulario</em><strong>]</strong><br />
Reemplace <em>fieldname</em> por el nombre de un campo en la tabla o consulta subyacente del informe que desea abrir. Sustituya <em>nombredeformulario</em> y <em>nombredecontrol en formulario</em> con el nombre del formulario y el control en el formulario que contenga el valor que quiere que coincidan en los registros del informe.</p>
<p><b>NOTA:</b>La longitud máxima del argumento Where Condition es de 255 caracteres. If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead. You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</p>
</td>
</tr>
<tr class="odd">
<td><p>Window Mode</p></td>
<td><p>Modo en el que se va a abrir el informe. Haga clic en <strong>Normal</strong>, <strong>Oculto</strong>, <strong>Icono</strong> o <strong>Cuadro de diálogo</strong> en el cuadro <strong>Modo de la ventana</strong>. El valor predeterminado es <strong>Normal</strong>.  </p>
<p><b>NOTA:</b>Algunas opciones de configuración de argumentos del Modo de ventana no se aplican al usar documentos con pestañas. Para cambiar a ventanas superpuestas:
<ol>
<li><p>Haga clic en <strong>Opciones</strong>.</p></li>
<li><p>En el cuadro de diálogo <strong>Opciones de Access</strong>, haga clic en <strong>Base de datos actual</strong>.</p></li>
<li><p>En la sección <strong>Opciones de aplicación</strong>, bajo <strong>Opciones de la ventana de documentos</strong>, haga clic en <strong>Ventanas superpuestas</strong>.</p></li>
<li><p>Haga <strong>clic en Aceptar</strong>y, a continuación, cierre y vuelva a abrir la base de datos.</p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

El valor **Imprimir** del argumento **Vista** imprime el informe de inmediato usando los valores de impresora actuales, sin que se muestre el cuadro de diálogo **Imprimir**. También puede usar la acción **AbrirInforme** para abrir y configurar un informe y usar, a continuación, la acción PrintOut para imprimirlo. Por ejemplo, cuando desea modificar el informe o usarla acción **Imprimir** para cambiar los valores de la impresora antes de imprimir.

El filtro y la condición WHERE aplicados se convertirán en el valor de la propiedad **Filtro** del informe.

La acción **AbrirInforme** es similar a hacer doble clic en el informe en el panel de navegación o hacer clic con el botón secundario en el informe en el panel de navegación y seleccionar una vista o el comando **Imprimir**.

> [!TIP] 
> - Si desea imprimir informes similares para diferentes conjuntos de datos, use un filtro o una cláusula WHERE para restringir los registros que se van a imprimir en el informe. A continuación, edite la macro para aplicar un filtro diferente o cambiar el argumento Where Condition.
> 
> - Puede arrastrar un informe desde el panel de navegación hasta una fila de acción de una macro. De este modo, se crea automáticamente una acción **AbrirInforme** que abre el informe en la vista Informe.

## <a name="example"></a>Ejemplo

El siguiente ejemplo nuestra cómo usar la acción OpenReport para pasar un parámetro que filtra un informe cuando se abre. El informe **rptChapters** muestra los registros del autor especificado al pasar el elemento seleccionado en el cuadro combinado **cboAuthors** al parámetro SelectedAuthor.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenReport
        Report Name rptChapters
        View Report
        Filter Name
        Where Condition
        Window Mode Normal
    
    Parameters
        SelectedAuthor =[cboAuthor]
```
