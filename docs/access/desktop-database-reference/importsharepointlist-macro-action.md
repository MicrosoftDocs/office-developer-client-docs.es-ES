---
title: ImportarListaDeSharePoint (acción de macro)
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e8b1e32eca6862645fc4f9c3b9021258e805dc8c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921323"
---
# <a name="importsharepointlist-macro-action"></a>ImportarListaDeSharePoint (acción de macro)

**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **ImportarListaDeSharePoint** para importar o vincular los datos de un sitio de Microsoft SharePoint Foundation.

> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.

## <a name="setting"></a>Configuración

La acción **ImportarListaDeSharePoint** tiene los siguientes argumentos.

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
<td><p><strong>Tipo de transferencia</strong></p></td>
<td><p>Seleccione el tipo de transferencia.</p>
<ul>
<li><p>Seleccione <strong>Importar</strong> para copiar los datos de Windows SharePoint Services a una tabla de Microsoft Access. Las actualizaciones a los datos de Access no afectan a los datos en Windows SharePoint Services. Del mismo modo, las actualizaciones a los datos de Windows SharePoint Services no afectan a los datos de Access.</p></li>
<li><p>Seleccione el <strong>vínculo</strong> para crear una tabla vinculada en Access que se vincula a los datos de SharePoint Foundation. Las actualizaciones a los datos de Access se reflejan en Windows SharePoint Services. Del mismo modo, las actualizaciones de los datos en Windows SharePoint Services se reflejan en Access.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Dirección del sitio</strong></p></td>
<td><p>Escriba la ruta de acceso completa al sitio de SharePoint.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Id. de lista</strong></p></td>
<td><p>Escriba el nombre o el identificador GUID de la lista que se va a transferir. Es un argumento obligatorio.</p></td>
</tr>
<tr class="even">
<td><p><strong>Id. de vista</strong></p></td>
<td><p>Escriba el identificador GUID de la vista de la lista que desee usar. Deje este argumento en blanco para transferir todas las filas y columnas de la lista.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nombre de la tabla</strong></p></td>
<td><p>Especifique el nombre que desee mostrar para la tabla o la tabla vinculada en Access.</p></td>
</tr>
<tr class="even">
<td><p><strong>Obtener valores de presentación de búsqueda</strong></p></td>
<td><p>Seleccione <strong>Sí</strong> para transferir los valores de presentación de los campos de búsqueda en vez del identificador usado para llevar a cabo la búsqueda.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

- Esta acción es lo mismo que hacer clic en **Lista de SharePoint** del grupo **Importar** en la ficha **Datos externos**. Los argumentos de la acción se corresponden con las opciones seleccionadas en el Asistente para obtener valores externos.

- Para ejecutar la acción **ImportarListaDeSharePoint** en un módulo de VBA, use el método **TransferSharePointList** del objeto **DoCmd**.

- Si especifica una lista o una vista inexistentes, no se producirán errores ni se transferirá ningún dato.

- Un identificador GUID es un identificador hexadecimal único de una lista o una vista. Dicho identificador debe especificarse en el formato siguiente, donde cada "F" es un número hexadecimal (del 0 al 9 o de la A a la F).
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  Para obtener el identificador GUID de una lista o una vista del sitio de SharePoint puede utilizar el procedimiento siguiente:
    
  1. Abra la lista de SharePoint Foundation.
    
  2. Si no se muestra la vista que desea, haga clic en la flecha desplegable **Ver** y, a continuación, seleccione la vista deseada.
    
  3. Haga clic en la flecha desplegable **Ver** y, a continuación, seleccione **Modificar esta vista**.La dirección de la barra de dirección del explorador contiene los identificadores tanto de la lista como de la vista. El identificador GUID de la lista sigue a **List=**, y el de la vista sigue a **View=**. Sin embargo, en la dirección, cada carácter **{** (abrir llave) se representa mediante la cadena **%7B**, cada carácter **-** (guión) mediante la cadena **%2D**, y cada carácter **}** (cerrar llave) mediante la cadena **%7D**. Por ejemplo:
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  Antes de poder usar los GUID de la dirección como argumentos de esta acción de macro, debe reemplazar cada cadena **7 ter %** con el carácter **{** , reemplace cada uno de ellos **% 2D** de la cadena con la **-** de carácter y reemplace cada cadena **% 7 D** con el carácter de **}** . No incluya el carácter **&** (y comercial) que sigue a la cadena **%7D** en el identificador GUID de la lista.

