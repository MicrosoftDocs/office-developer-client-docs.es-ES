---
title: NuevaConsulta (acción de macro)
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a0f951c69939e8265bab64193e594eed32149c38
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920035"
---
# <a name="requery-macro-action"></a>NuevaConsulta (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **NuevaConsulta** para actualizar los datos de un control especificado del objeto activo consultando de nuevo el origen del control. Si no se especifica ningún control, con esta acción se vuelve a consultar el origen del propio objeto. Utilice esta acción para asegurarse de que el objeto activo o uno de sus controles muestra los datos más actualizados.

## <a name="setting"></a>Configuración

La acción **NuevaConsulta** tiene el siguiente argumento.

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
<td><p><strong>Nombre del control</strong></p></td>
<td><p>Nombre del control que se desea actualizar. Escriba el nombre del control en el cuadro <strong>Nombre del control</strong> de la sección <strong>Argumentos de acción</strong> en el panel Generador de macros. Sólo debe utilizar el nombre del control y no el identificador completo (como <strong>Formularios</strong>!<em>nombreDelFormulario</em>!<em>nombreDelControl</em>). Deje este argumento en blanco para consultar de nuevo el origen del objeto activo. Si el objeto activo es una hoja de datos o un conjunto de resultados de una consulta, debe dejar este argumento en blanco.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La acción **NuevaConsulta** realiza alguna de las siguientes acciones:

  - Ejecuta de nuevo la consulta en la que está basada el control o el objeto.

  - Presenta cualquier registro nuevo o modificado y quita cualquier registro eliminado de la tabla en la que está basado el control o el objeto.


> [!NOTE]
> <P>[!NOTA] La acción <STRONG>NuevaConsulta</STRONG> no afecta a la posición del puntero de registro.</P>



Los controles basados en una consulta o tabla son:

  - Cuadros de lista y cuadros combinados.

  - Controles de subformulario.

  - Objetos OLE, por ejemplo, gráficos.

  - Controles que contienen funciones de agregado de dominio, como **DSuma**.

Si el control especificado no está basado en una consulta o tabla, esta acción hace que se vuelva a calcular el control.

Si deja en blanco el argumento **Nombre del control**, la acción **NuevaConsulta** tiene el mismo efecto que presionar MAYÚS+F9 cuando el objeto tiene el enfoque. Si un control de subformulario tiene el enfoque, esta acción vuelve a consultar sólo el origen del subformulario (al igual que cuando se presionan MAYÚS+F9).


> [!NOTE]
> <P>[!NOTA] La acción <STRONG>NuevaConsulta</STRONG> vuelve a consultar el origen del control u objeto. En cambio, la acción <STRONG>RepintarObjeto</STRONG> vuelve a pintar los controles del objeto especificado pero no vuelve a consultar la base de datos ni muestra los nuevos registros. La acción <STRONG>MostrarTodosRegistros</STRONG> no sólo vuelve a consultar el objeto activo sino que también quita todos los filtros que se hayan aplicado, a diferencia de la acción <STRONG>NuevaConsulta</STRONG>.</P>



Si desea volver a consultar un control que no esté en el objeto activo, deberá utilizar el método **Requery** en un módulo de Visual Basic para Aplicaciones (VBA), en lugar de la acción **NuevaConsulta** o su correspondiente método **Requery** del objeto **DoCmd**. El método **Requery** en VBA es más rápido que la acción **NuevaConsulta** o el método **DoCmd.Requery**. Además, cuando se utiliza la acción **NuevaConsulta** o el método **DoCmd.Requery**, Microsoft Access cierra la consulta y vuelve a cargarla desde la base de datos, pero cuando se utiliza el método **Requery**, Access ejecuta de nuevo la consulta sin cerrarla ni cargarla. Tenga en cuenta que el objeto de datos ActiveX (ADO) **Requery** (método) funciona de la misma manera que el método **Requery** de de Access.

