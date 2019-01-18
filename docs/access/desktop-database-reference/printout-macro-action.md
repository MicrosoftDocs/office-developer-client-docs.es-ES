---
title: Imprimir (acción de macro)
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 04212a8bf63d5039c6548463612f006f0d116229
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718598"
---
# <a name="printout-macro-action"></a>Imprimir (acción de macro)

**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **Imprimir** para imprimir el objeto activo de la base de datos abierta. Puede imprimir hojas de datos, informes, formularios, páginas de acceso a datos y módulos.

> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **Imprimir** tiene los siguientes argumentos.

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
<td><p><strong>Intervalo de impresión</strong></p></td>
<td><p>Intervalo que se va a imprimir. Haga clic en <strong>Todo</strong> (el usuario puede imprimir todo el objeto), <strong>Selección</strong> (el usuario puede imprimir la parte del objeto que se haya seleccionado) o <strong>Páginas</strong> (el usuario puede especificar un intervalo de páginas en los argumentos <strong>Desde la página</strong> y <strong>Hasta la página</strong>) en el cuadro <strong>Intervalo de impresión</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. El valor predeterminado es <strong>Todo</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Desde página</strong></p></td>
<td><p>Primera página que se va a imprimir. La impresión comienza al principio de esta página. Este argumento es obligatorio si se selecciona <strong>Páginas</strong> en el cuadro <strong>Intervalo de impresión</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Hasta página</strong></p></td>
<td><p>Última página que se va a imprimir. La impresión se detiene en la parte inferior de esta página. Este argumento es obligatorio si se selecciona <strong>Páginas</strong> en el cuadro <strong>Intervalo de impresión</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Calidad de impresión</strong></p></td>
<td><p>Calidad de la impresión. Haga clic en <strong>Alta</strong>, <strong>Media</strong>, <strong>Baja</strong> o <strong>Borrador</strong>. Cuanto menor sea la calidad, más rápido se imprimirá el objeto. El valor predeterminado es <strong>Alta</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Copies</strong></p></td>
<td><p>Número de copias que se va a imprimir. El valor predeterminado es 1.</p></td>
</tr>
<tr class="even">
<td><p><strong>Intercalar copias</strong></p></td>
<td><p>Haga clic en <strong>Sí</strong> (para intercalar las copias impresas) o en <strong>No</strong> (para no intercalar las copias). El objeto se imprime más rápido si este argumento está establecido en <strong>No</strong>. El valor predeterminado es <strong>Sí</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Esta acción es similar a seleccionar un objeto, hacer clic en la pestaña **Archivo** y, a continuación, hacer clic en **Imprimir**. Con esta acción, no obstante, no aparece el cuadro de diálogo **Imprimir**.

> [!TIP]
> [!SUGERENCIA] Si utiliza frecuentemente determinados valores de impresión, cree una macro que contenga una acción **Imprimir** con esos valores en sus argumentos.

Los argumentos de esta acción corresponden a las opciones del cuadro de diálogo **Imprimir**. No obstante, a diferencia de la acción **BuscarRegistro** y del cuadro de diálogo **Buscar y reemplazar**, los valores de los argumentos no se comparten con las opciones del cuadro de diálogo **Imprimir**.

Para ejecutar la acción **Imprimir** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **PrintOut** del objeto **DoCmd**.

