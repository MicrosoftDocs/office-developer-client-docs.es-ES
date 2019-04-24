---
title: EstablecerFiltro (acción de macro)
TOCTitle: SetFilter macro action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ac1a2c8a603fb74b56d71f73605455ecdbc87035
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308697"
---
# <a name="setfilter-macro-action"></a>EstablecerFiltro (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede utilizar la acción **EstablecerFiltro** para aplicar un filtro a los registros de la hoja de datos, formulario, informe o tabla que esté activo.

## <a name="setting"></a>Configuración

La acción **EstablecerFiltro** utiliza los siguientes argumentos.

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
<td><p>Nombre del filtro</p></td>
<td><p>Si se proporciona, el nombre de una consulta o de un filtro guardado como consulta. Este argumento o el argumento CondiciónWhere es necesario en una base de datos cliente. En una base de datos Web, este argumento no está disponible.</p></td>
</tr>
<tr class="even">
<td><p>Condición WHERE</p></td>
<td><p>Si se proporciona, una cláusula WHERE de SQL que restringe los registros en la hoja de datos, formulario, informe o tabla. En una base de datos Web, este argumento es obligatorio.</p></td>
</tr>
<tr class="odd">
<td><p>Nombre del control</p></td>
<td><p>Si se proporciona, es el nombre del control que corresponde al subformulario o subinforme que se va a filtrar. Si está vacío, se filtra el objeto actual.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

En una base de datos web, el argumento Condición WHERE no puede empezar con un signo igual (=).

Al ejecutar esta acción, el filtro se aplica a la tabla, formulario, informe u hoja de datos (por ejemplo, el resultado de consulta) que está activo y tiene el enfoque.

La propiedad **Filtro** del objeto activo se utiliza para guardar el argumento CondiciónWhere y aplicarlo en un momento posterior. Los filtros se guardan con los objetos en los que se crean. Se cargan automáticamente cuando se abre el objeto, pero no se aplican automáticamente.

En una base de datos cliente, para aplicar un filtro automáticamente cuando se abre el objeto, establezca la propiedad **FiltrarAlCargar** en Verdadero.

En una base de datos web, para aplicar un filtro cuando se abre el objeto, agregue la acción **EstablecerFiltro** a una macro y agregue la macro al evento **AlCargar ** del objeto.

## <a name="example"></a>Ejemplo

En el siguiente ejemplo, se muestra cómo usar la acción SetFilter para filtrar el formulario en el que se define la macro.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
