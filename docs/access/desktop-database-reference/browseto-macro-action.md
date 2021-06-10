---
title: Explorar (acción de macro)
TOCTitle: BrowseTo macro action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bcf0a37f8c1596856f5d7b921430371d620f7a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296776"
---
# <a name="browseto-macro-action"></a>Explorar (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede utilizar la acción **Explorar** para desplazarse entre objetos en su lugar. También puede cambiar el objeto de origen de un control de subformulario especificando el argumento Ruta de acceso al control de subformulario. Utilice la acción **Explorar** para desplazarse de formulario1 a formulario2 sin abrir una ventana nueva.

## <a name="setting"></a>Configuración

La acción **Explorar** tiene el siguiente argumento.

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
<td><p>Tipo de objeto</p></td>
<td><p>El tipo de objeto en el que se va a explorar.</p></td>
</tr>
<tr class="even">
<td><p>Nombre de objeto</p></td>
<td><p>El objeto que se carga dentro del control de subformulario al que hace referencia al argumento Ruta de acceso al control de subformulario.</p></td>
</tr>
<tr class="odd">
<td><p>Ruta de acceso al control de subformulario</p></td>
<td><p>Si se especifica, la ruta de acceso desde la forma principal de la aplicación al control de subformulario de destino que carga el objeto especificado por el argumento Nombre de objeto.</p></td>
</tr>
<tr class="even">
<td><p>Condición WHERE</p></td>
<td><p>Si se especifica, reemplaza la condición WHERE del origen de registro de objeto.</p></td>
</tr>
<tr class="odd">
<td><p>Page</p></td>
<td><p>Si especifica, se establece la página del formulario continuo que se realizarán la página actual. Este argumento es solo web.</p></td>
</tr>
<tr class="even">
<td><p>Modo de datos</p></td>
<td><p>Si se especifica, es el modo de entrada de datos del formulario.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

El argumento Ruta de acceso al control de subformulario debe especificarse mediante la sintaxis en el ejemplo de código siguiente:

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

En este ejemplo, el formulario principal es el formulario de nivel superior en la aplicación de cliente de Access. El argumento Ruta de acceso al control de subformulario debe especificar alternativamente los nombres de control de formulario y subformulario que van del formulario principal al control de subformulario que es el contenedor del objeto especificado por el argumento Nombre de objeto. Cada control del subformulario especificado debe ser un control en el formulario que lo precede. La ruta de acceso debe terminar con un control de subformulario.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar la acción BrowseTo para abrir un informe en un control de subformulario o dentro de un control de navegación.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OnError
        Go to Next
        Macro Name
    
    /* Try to load the report in the host form (frmAuthorsParameter)    */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
    
    /* if this fails, try to load it in the navigation subform     */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmMain.NavigationSubform>frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
```



